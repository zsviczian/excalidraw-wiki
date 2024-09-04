This is an absolutely must read resource: [https://www.moritzjung.dev/obsidian-collection/plugin-dev/debuggingandprofiling/](https://www.moritzjung.dev/obsidian-collection/plugin-dev/debuggingandprofiling/ "https://www.moritzjung.dev/obsidian-collection/plugin-dev/debuggingandprofiling/")
Plus this [article](https://alan.norbauer.com/articles/browser-debugging-tricks)by [Fevol](https://github.com/Fevol)

On top of those above, I've implemented the following in the Excalidraw plugin:

In my main Plugin class I overrode registerEvent to monitor duration of events:
```typescript
export default class ExcalidrawPlugin extends Plugin {
//....
  public registerEvent(event: any) {
    if(!isDebugMode) {
      super.registerEvent(event);
      return;
    }

    const originalHandler = event.fn;

    // Wrap the original event handler
    const wrappedHandler = async (...args: any[]) => {
      const startTime = performance.now(); // Get start time
  
      // Invoke the original event handler
      const result = await originalHandler(...args);
  
      const endTime = performance.now(); // Get end time
      const executionTime = endTime - startTime;
  
      if(executionTime > durationTreshold) {
        console.log(`Excalidraw Event '${event.name}' took ${executionTime}ms to execute`);
      }
  
      return result;
    };
  
    // Replace the original event handler with the wrapped one
    event.fn = wrappedHandler;
  
    // Register the modified event
    super.registerEvent(event);
  }
```

And I created a DebugHelper.ts that includes a wrapper for MutationObservers - I have couple of those in the code - and those can become resource-intensive.
```typescript
export const isDebugMode = true;
export const durationTreshold = 2; //ms

export class CustomMutationObserver {
  private originalCallback: MutationCallback;
  private observer: MutationObserver | null;
  private name: string;

  constructor(callback: MutationCallback, name: string) {
    this.originalCallback = callback;
    this.observer = null;
    this.name = name;
  }

  observe(target: Node, options: MutationObserverInit) {
    const wrappedCallback: MutationCallback = async (mutationsList, observer) => {
      const startTime = performance.now(); // Get start time
      await this.originalCallback(mutationsList, observer); // Invoke the original callback
      const endTime = performance.now(); // Get end time
      const executionTime = endTime - startTime;
      if (executionTime > durationTreshold) {
        console.log(`Excalidraw ${this.name} MutationObserver callback took ${executionTime}ms to execute`);
      }
    };

    this.observer = new MutationObserver(wrappedCallback);

    // Start observing with the modified callback
    this.observer.observe(target, options);
  }

  disconnect() {
    if (this.observer) {
      this.observer.disconnect();
      this.observer = null;
    }
  }
}
```

And here's how I modified my mutation observers' declarations:

```typescript
export const observer = isDebugMode
  ? new CustomMutationObserver(legacyExcalidrawPopoverObserverFn, "legacyExcalidrawPopoverObserverFn")
  : new MutationObserver(legacyExcalidrawPopoverObserverFn);
```