---
aliases:
  - WIKI/03+Advanced+Usage/Publish+js+and+css+files
permalink: wiki/publish/setup
---
Create two files in your vault root: `publish.css` and `publish.js`. These files won't be editable inside Obsidian, unless you install a dedicated plugin for that. Use an external text editor to edit the files. You can also download these files from [here](https://gist.github.com/zsviczian/0bb31aa2d08ba689c14158e82cbbda5a)
# publish.css
```css
@font-face {font-family: "Virgil";src: url("https://excalidraw.com/Virgil.woff2");}
@font-face {font-family: "Cascadia";src: url("https://excalidraw.com/Cascadia.woff2");}
@font-face {font-family: "Assistant";src: url("https://excalidraw.com/Assistant-Regular.woff2");}

div.markdown-embed-title {
  display: none;
}

div.markdown-embed {
  border: none;
  padding: 0px;
  background-color: inherit;
}

div.excalidraw-svg {
	/*width: fit-content;*/
	height: 100%;
}

svg.excalidraw-svg {
	max-width:100%;
	max-height: 90vh;
	width: var(--page-width);
}

svg.excalidraw-svg.ex-pageheight {
	width: initial;
	height: 100%;
}

svg.excalidraw-svg.ex-pagewidth {
	width: 90vw;
	height: initial;
}

.excalidraw-svg .text {
  width: 100%;
  text-align: center;
}

div.excalidraw-svg.enlarged {
    position: fixed;
    top: 0;
    left: 0;
    z-index: 10;
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

body {
	--background-primary: #FFF6F0;
}

a.site-body-left-column-site-name {
	display: none;
}

div.site-footer {
	display: none;
}
```

# Publish.js
```js
const clickToEnlarge = "Click and hold to enlarge. SHIFT + wheel to zoom. ESC to reset.";
const clickToCollapse = "ESC to reset. Click and hold to collapse. SHIFT + wheel to zoom";

//check if in iFrame - if yes the page is assumed to be an embedded frame
if(window.self !== window.top) {
  const elements = [
    "div.site-body-right-column",
    "div.site-body-left-column",
    "div.site-header",
    "div.site-footer"
  ];
  elements.forEach(x=>{
    document.querySelectorAll(x).forEach(div=>{
      div.style.display = "none";
    });
  });
}

const baseUrl = `${window.location.origin}/`;

const [isDesktop, isMobile, isTablet] = (()=>{
  const userAgent = navigator.userAgent;
  const mobileKeywords = ['Mobile', 'Android', 'iPhone', 'iPad', 'Windows Phone'];

  const isMobile = mobileKeywords.some(keyword => userAgent.includes(keyword));
  const isTablet = /iPad/i.test(userAgent) || (isMobile && !/Mobile/i.test(userAgent));
  const isDesktop = !isMobile && !isTablet;

  return [isDesktop, isMobile, isTablet];
})();

const addNavigationToDiv = (container) => {
  const svgElement = container?.querySelector('.excalidraw-svg');
  if(!svgElement) return;
  container.addClass("excalidraw-svg");
  svgElement.removeAttribute("width");
  svgElement.removeAttribute("height");
  
  if(!isDesktop) return;
  
  const textDiv = document.createElement('div');
  textDiv.className = 'text';
  textDiv.textContent = clickToEnlarge;
  container.appendChild(textDiv);

  let isEnlarged = false;
  let timeout = null;
  let isReadyToPan = false;
  let isPanning = false;
  let zoomLevel = 1;
  let panX = 0;
  let panY = 0;
  let pinchStartDistance = 0;
  let panStartX = 0;
  let panStartY = 0;

  const clearEnlargeTimeout = () => {
    if(timeout) clearTimeout(timeout);
    timeout = null;
  }

  const enablePointerEvents = (val) => {
    svgElement.querySelectorAll("a").forEach(el=>{
      el.style.pointerEvents = val ? "all" : "none";
    });
  }

  const applyTransform = () => {
    svgElement.style.transform = `scale(${zoomLevel}) translate(${panX}px, ${panY}px)`;
    clearEnlargeTimeout();
  };

  //Wheel zoom
  svgElement.addEventListener('wheel', (event) => {
    if(!event.shiftKey ) return;
    if (event.deltaY > 0) {
    zoomLevel -= zoomLevel > 4 
	  ? (zoomLevel > 6 
	    ? (zoomLevel > 10 ? 0.4 : 0.3)
		: 0.2) 
	  : 0.1;
    } else {
    zoomLevel += zoomLevel > 4 
	  ? (zoomLevel > 6 
	    ? (zoomLevel > 10 ? 0.4 : 0.3)
		: 0.2) 
	  : 0.1;
    }
    applyTransform();
  });

  // Panning
  svgElement.addEventListener('mousedown', (event) => {
    isReadyToPan = true;
    panStartX = event.clientX;
    panStartY = event.clientY;
  });

  svgElement.addEventListener('mousemove', (event) => {
    const deltaX = event.clientX - panStartX;
    const deltaY = event.clientY - panStartY;
    const distance = Math.sqrt(deltaX**2+deltaY**2);
    if (isReadyToPan && (distance > 20)) {
      if(!isPanning) {
        enablePointerEvents(false);
        isPanning = true;
      }
      panX += deltaX/zoomLevel;
      panY += deltaY/zoomLevel;
      panStartX = event.clientX;
      panStartY = event.clientY;

      applyTransform();
    }
  });

  svgElement.addEventListener('mouseup', () => {
    enablePointerEvents(true);
    isPanning = false;
    isReadyToPan = false;
  });

  svgElement.addEventListener('mouseleave', () => {
    enablePointerEvents(true);
    isPanning = false;
    isReadyToPan = false;
  });

  //abort on Escape
  document.addEventListener('keydown', (event) => {
    if (event.key === 'Escape') {
      enablePointerEvents(true);
      isEnlarged = false;
      isPanning = false;
      isReadyToPan = false;
      container.classList.remove("enlarged");
      textDiv.textContent = clickToEnlarge;
      zoomLevel = 1;
      panX = 0;
      panY = 0;
      applyTransform();
    }
  });
 

  //Enlarge on long click
  svgElement.addEventListener('mouseup', () => clearEnlargeTimeout());
  svgElement.addEventListener('mousedown', () => {
    timeout = setTimeout(()=> {
      timeout = null;
      if(isPanning) return;
      isReadyToPan = false;
      if (isEnlarged) {
        // Collapse the image
        container.classList.remove("enlarged");
        textDiv.textContent = clickToEnlarge;
      } else {
        // Enlarge the image
        container.addClass("enlarged");
        textDiv.textContent = clickToCollapse;
      }
      isEnlarged = !isEnlarged;
    },1000);
  });

  applyTransform();
}

const processIMG = (img) => {
  const svgURL = img.src;
  const container = img.parentElement;

  fetch(svgURL)
    .then((response) => {
      if (response.ok) {
        return response.text();
      }
      throw new Error('Failed to fetch SVG');
    })
    .then((svgContent) => {    
      svgContainer = document.createElement('div');
      svgContainer.innerHTML = svgContent;
      svgContainer.querySelectorAll(`a[href^="obsidian://open?vault="`).forEach(el=>{
        el.setAttribute("href",unescape(el.getAttribute("href").replace(/.*&file=/,baseUrl).replaceAll(" ","+")));
      });
      svgContainer.querySelectorAll(`iframe[src^="obsidian://open?vault="`).forEach(el=>{
        el.setAttribute("src",unescape(el.getAttribute("src").replace(/.*&file=/,baseUrl).replaceAll(" ","+")));
      });
      container.removeChild(img);
      container.appendChild(svgContainer);
      addNavigationToDiv(svgContainer);
      
    })
    .catch((error) => {
      console.error('Error: ' + error);
    });
}

const addImgMutationObserver = () => {
  const targetElement = document.body;
  const handleImgAddition = (mutationsList, observer) => {
    for (const mutation of mutationsList) {
      if (mutation.type === 'childList') {
    mutation.addedNodes.forEach(node => {
      if (node instanceof Element && node.querySelector(`img[alt$=".svg"]`)) {
        processIMG(node.querySelector(`img[alt$=".svg"]`));
      };
        });
      }
    }
  }
  const observer = new MutationObserver(handleImgAddition);
  const config = { childList: true, subtree: true };
  observer.observe(targetElement, config);
}

//process images after loading
document.body.querySelectorAll(`img[alt$=".svg"`).forEach(img => {
  processIMG(img);
});

addImgMutationObserver();
```