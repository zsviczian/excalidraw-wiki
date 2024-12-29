---
excalidraw-plugin: parsed
tags:
  - excalidraw
excalidraw-autoexport: svg
excalidraw-open-md: true
aliases:
  - WIKI/03+Advanced+Usage/Color+Palette
permalink: wiki/color-palette
---
# [[WIKI/03 Advanced Usage/Color Palette]]
You can define your custom color palettes. The steps are a bit technical, however, once you've set up the Color Palette, you can [[Create your Template]], load the palette to the template, and all your new Excalidraw documents will have your custom color palette.

You will find the [Palette Loader Script](https://github.com/zsviczian/obsidian-excalidraw-plugin/blob/master/ea-scripts/Palette%20loader.md) in the Excalidraw Automate [[Script Library]].

These two videos explain how to set up a color palette:
![Color Picker](https://youtu.be/diBT5iaoAYo)

Link:: [Color Picker Video](https://youtu.be/diBT5iaoAYo)

![Palette Loader](https://youtu.be/epYNx2FSf2w)

Link:: [Palette Loader Video](https://youtu.be/epYNx2FSf2w)
## Structure of the palette file
Here's a sample palette file. The 6 digit hexadecimal values listed one after the other in new rows are the colors. Notice how they are in batches of 5, matching the palette in Excalidraw. Notice also that the numbers do not have the "#" sign at the front.

There are two things you need to understand about the sequence of the colors.
- The first batch is the first row of colors in the picker, the second the second, etc. You can have as many batches as you'd like.
- The batches of 5 are tricky. Colors are in the order of 3-1-2-4-5, that is, the middle color is the first in the sequence. The strange sequence has historical reasons... now, it cannot be changed else impacting backwards compatibility.

Notice also that you can add lines with non-color codes to your file. Palette Loader will skip these. You can use these lines to store the original palette definition should you need to go back to it later.
```
source:: [Paletton Palette](https://paletton.com/#uid=43j0t0kpSAtfHMQl6FTy1xHyjol)
22A5AB
6CCED2
41B7BC
01989F
017075

FFBA31
FFD582
FFC757
FFAA00
C28100

FF3B31
FF8882
FF5F57
FF0D00
C20A00

FF9031
FFBC82
FFA557
FF7600
C25A00
```

The palette in the file above looks like this:
![[Screenshot - Demo Palette.png|200]]

The colors in the first row of the palette are automatically generated. The two grays are tinted based on the middle color of the first first row of your palette: "d" in the screenshot above.

### The Palettes Folder
The palette file is a simple markdown file placed in the Palettes Folder. By Default it is the `Excalidraw/Palettes` folder. After downloading the [[Palette Loader Script]] you need to run it from Obsidian Command Palette. At the first run, the script will register a custom settings section at the bottom of Excalidraw Plugin Settings. You may configure the palette folder here. Note, that foler names are CasE seNSitIVe. You may also define the light and dark gray values used by the script to create the tinted grays in the palette as mentioned above.

![[Screenshot - Plugin Settings - Palette Loader Settings.jpeg]]
## Designing your Palette
You can design your palette at http://paletton.com/
![[Screenshot - Paletton Config Screen.jpeg]]

Once you are happy with the colors you need to export the palette. 

The easiest option is to click Tables/Export in the bottom right of the screen - **However, unfortunately, this feature often does not work :(** If you run into issues you'll find alternative approaches further below

1) Click the "Tables/Export" button as shown on the screenshot above.
2) On the next screen click "as text". You will need to manually delete "#" from the exported values, and format the file to match the example above, but it only takes a minute.

![[Screenshot - Paletton Export Screen.jpeg]]
### In case "as text" does not work
You have two options in case "as text" does not work.
#### Option 1 - Manually copy values into a text file
Open a new note in Obsidian and type in the values from the export screen. Don't forget, in each row the middle value comes first, then the first, second, fourth and fifth. This should take no more than 5 minutes.

#### Option 2 - Use script to extract the values
If you are comfortable with scripting you can follow the below approach. However, note, that sometimes the structure of the Paletton page changes, in this case you may need to tweak the code a bit.

![[Screenshot - Paletton Export with Code.jpeg]]

0. On the palette configuration page press CTRL+SHIFT+i or (CMD+OPT+i on a Mac).
1. Click "Console"
2. Paste the below script. Note, if you have not pasted script to console before you will be prompted with a warning. You need to type: "allow pasting".
3. Paste the code and run it. If you run into an error, then Paletton has likely changed something. You can try to figure out the change using the Elements browser. At this point your on your own. You are probably better off manually copying the values to a text file as per the previous point.
4. Select the result, copy it to the clipboard and paste it to your palette file in Obsidian.

Here's the script you want to run:
```javascript
s=`source:: [Paletton Palette](${window.location.href})`;
document
  .querySelector(".pane.pane-palette")
  .querySelectorAll("[title]")
  .forEach((x,i)=>{
    s += `\n${x.getAttribute("title")}`;
    if((i+1)%5===0) s+="\n";
  })
console.log(s)
```

## The Excalidraw appState Custom Palette Data Object
The Excalidraw drawing is stored in a JSON data structure under Excalidraw Data / Drawing. You can find this JSON by switching to [[Markdown View]] and selecting [[Decompress current Excalidraw File]] from the Obsidian Command Palette (in case you see [[compressed-json]] in the [[Drawing Section]] of the file).

The color palette is at the end of the JSON in the `appState` section. This is its structure:

```js
colorPalette: {
  canvasBackground: [string, string, string, string, string][] | string[],
  elementBackground: [string, string, string, string, string][] | string[],
  elementStroke: [string, string, string, string, string][] | string[],
  topPicks: {
    canvasBackground: [string, string, string, string, string],
    elementStroke: [string, string, string, string, string],
    elementBackground: [string, string, string, string, string] 
  },
}
```

Finally there is a GitHub Gist with the code. In case of questions you might find answers [here](https://gist.github.com/zsviczian/28b0864569ae50a59a65c3bd23e35c1a)

%%
# Excalidraw Data

## Text Elements
## Drawing
```compressed-json
N4KAkARALgngDgUwgLgAQQQDwMYEMA2AlgCYBOuA7hADTgQBuCpAzoQPYB2KqATLZMzYBXUtiRoIACyhQ4zZAHoFAc0JRJQgEYA6bGwC2CgF7N6hbEcK4OCtptbErHALRY8RMpWdx8Q1TdIEfARcZgRmBShcZQUebQB2bQAWGjoghH0EDihmbgBtAF1+CFw4OABlKKhxVFAwSHUMmogiZWlU+oZCBAoAIVxsAGtlUmEOYgBhNnw2Um4IAGIAMRWA

NiWABg7IbBFA7IBJav1K0cGEKZm5iQWARgR7++2IXdJ9qCOM/qGRscnp2bzKDkDjMOC4d7PV7vT76JaEfD4SowYLzQQeKF7LIfY6nNjnADqJHU3D44B2WMOuOB+IQyNREnRJExb2xsIASsI2hxwrk0Ld+BTWVSMgB5cHYNQwbi3DYbQUvSk4jJLThQJa4fQI6VoACsCuhbOOquy5UIRhqt1WBqVsIAKlgoABBVpcCTBABmUBZMOpEOdbzYFEkIWI

3A4QkRNuFyv0AFFxk7A8HQ/MIaMqNHfRkkxm7fBmqMhONnsxsKNEQANbirVYATm0PH15IgZYr+AAmtwknW4s3OkY2AZuHVOvQCEJLeSAL5Zo0ZTnF4g85h89BFksKkYkM0W0nylvb4iVBBwbj9yBHgCybGICATuE0wTDaA9BDCW9IJEugLQo8gvTTC+67KJouAABTxEk1CoPE8QwVaAqoBs2i6gAlNskDsggyiRhC8ykKBEG6gAHDBqzyqgtw8Na

yGoRhM4GgCpAAAoEAgMg1P+LzWOOzDfMMG7AXk5KdMC1hghC2KYZAT4DIMMkifUymLKsSSrDRtwyZACy9DwvQbAZ2mLCRvQkXWJEkcZCwAMw8DZtwOdZtx1i5txWaJYBFJ5SnKTpExxhMAAiEwTNZcarBFca6tZQVOnFQV1tZ9arPEanWTZSQ2dlPAQJ53l+RAwZqEggr1L5KnLGsmzWSsSy9EsVllZ0VWNUsKTNTpjWrDZcrWfEEx2X1+XNRVLU

RUFPATFpnWLEsNlxnWcZbLNCyBUFG0zZ5Ol1mlPVBdZSS9NltxxnlfkFcpY06U6SyufETXbYsQUDaZvTWYNToTHWTrWbqQVJCRNnxNZPBxjwSS3O9I0+U9CzxLqup1pDH1JE6vR1qs1lOg9iEZXpk1bX5Om3EFiFbDDfnXYspEObcROFQsQWLTZiPY0FFE8AzlVTe5GxJatVobBMGwpJTV1w3WdbM8zH0BUscZLNZx1RVjq1gyRcaa85UG6+dymX

eVcM2SR6Po9ZyMhSFf1LBMvR285Ey6qszvWRs4N6dDF2jXDcpS1Lh1BXVSurXKSw8OHbuiwDB2hxsNE0fr9SG2A1MLHKta1hlNnB1HoWhVH2XZVHblJeLRvE4scpTVNznrHVUdOhsTcl6sVpR4ZhlJ15PuVwsExLEF/0xatcbxHGToT7FvTLctyU8PEGyLxljlAx53uw33UGm6byt1k7TsW/EOM4xlTpJLqF/OZNdk2d3Kdp4DKUC5Ldu9O/yUY/

7oNZbqrPOVzJ0txfrl1TnDBe6l1L9TjL0eIsDDpmVWCRNWcNbhJHsvZN2QCua5VAWnZurN/6rSylbMKgtvo2TrHfUOuooZQzdr1IKGwDp4LhisAyRlVorBei9WqtskgTA6nDIKJE5R9VWqsEWYj7690ZisP+f8+FOh+i/PuKxx7j2xnWMRK04aXx0TIzecjNjSK4Y1DYoi+FJFFrovuoiDHEJ0RTDeVM4ZOibqYthSxEZszMQ4vRup/F9x4B44aL

iJZ9zRkE4xTYmzK0Xp44JgTEmM2ogY1hajB5HVscYievCzFB0EbFZBPBxFw0kQ5MJBtZGVRWEAxRBTm6qOMRjTRq1lFJCYTkyql8aJVOTjUlq6jrHdKGfVJ0lizG7WsdZURNkPGHQ2KTfpPcjGVXcZ0spmSnRNhHl4+IvVRk6URn0o5iwQmORWQ/OGaMuZbOMSUvZfdYG6lKWchYTZ6b3Mqmk+xhjXGZOipwrx4d8leMCkU1aIjXLfJapIwGVzBl

dVti7ah4L5nNNqVktpbjdqyneZfE2iK1ljPcbC5FANJleIajM1aojEbksWNY/SxKAWM3cfEN5fCJgIyecY9GjKFiI0oYKi5Uj/kRMZmjSp7z2GvL5ZVWB8RtHvM+SqgBwsrmiUNhgYImRTQ0nOPkTy0AQSSUhM1CAckhiKThp7TusyzIWUen3W+jluYtVLu5ZK6lNISorozVW0VYrxXipiuFmM0pCNdVlHKH11oF1AUVSQJVbWZPqo1PhbVo1yOQ

Yc/qg0uVmKWOsZx1SSVdQWktd561NpH1rDZWONzjoOTOqPVYk1pr+rAX3F6Ew3ofXmd9X6q1/qA2BqDcGkN3rtLurcB63a06CPRpjbGuM274x4ITa+5N+qI2RlpDJjNmZUN8W4jm8cPU6V5qI8NJMKIixzT0oG9ND3hIDZVUKitFbKwWpFFBwStZAZ1kkPWq0pYyzOkeyqltgpkL0bbe2M7UFOxdgBxm7t9L6QyqbXo5toMtU6bnOO4dI5x06Z0q

OCd0OVT9t/AjOlsrEd9sLfOhci4l1cnequGxM5YwY4sK0zG+5yibi3OOiEaMtTERwqjExa4CbWuPSeI7hEz3du8jSi9l6rQcibE2H1B7D0XXa/eupD7gePlZs+F8r6Cxvpg1a28JkgPfT2xm+934fwkV/AO6tf5ENQYA4Bh1kGYzLm5tO49YHwOIYg5Bzl0G3ywdRaioMoJqX45Fm5ja4OOyoVQt2tDej0NDow5hWDCExUU9w+IYLMmCMhcI+xgr

JHRKxRwstAyK1zSWMo5RfCNFttxe1lq+iUlYoUXfGr5iqWZOsbSuGLXBUjIm2M9J2XMk+IVettbxzkmitCe8sl0iZuxJ2zpWBo3r0HfeWkvbTKjsmcBfFEGBT+HFI0q1wa+K+EAyMjNphA2zGtOG33DpXS/roIorKvrtxFEzbw3N4x0z3lzIWY45ZsOoKsslVinZZ7MkHMFScmHoMgH5vaefSHM3HnxNeaK2hv3BalL+cQnZv2Zugre+C0KT6WrQ

uZ+UwRbPwW6gB5t3JGK/ugbB+yvFJOsqi4a6i57xjKWw5pWjjYDL3nMoMrDk7ausU8sJ/yg3f0/7qvVkA8VVPOW44/WM3o8r4nKsZy5QVaS7c3KdDK++2qyq6qaNkASvwlzGsKuJUE4ILUmutQpJFix7XAr7plv1dKnWWQyvZd1zkuPesU0Gi7iwApwfg720NiVkqRvSrp2Ndlu3JtTUn1qDUXXGJLTVYtJF2q1TzYKgaQ0uurLZbUqtc922dqvY

sWtZN637QQSdKDkvKp9oHbO+6HfP1Dp+n9SlE71ZTvoYp5dGMpM6V5QetdJE8a6YJlzHdbcR/XN7SzM3z66Yz4WPFTm3+b38x1yapiyr4tRfoKwhySzSxxiyyrQqz/qTqazayCy6ygbG4tSwbWy6a4bmyjqIYOzkLOyuyhwezYaKZEYNxxz+zcbpwbCka5TkYxxUYaRZblpj4tRMaUEsZ8Z5xsZxxFxooiZLJcboH3rCYYbxzyYV4SFibvJyiSYd

yyZF7KZTyrQDxDxDzTyzyaYLxLzvJ6ZryiHJ5mYWZwzOa7yWYnw86urnyXwl53AObTagE7RvzeY3Jhb1ifzUE/xVYALAIhaKbRZwLWGMwQKZYILIIJaCxJaOa+zYJpbkG5ZYFxG+HkIFaCEYbFala+zlYsLOG9Y8IhEdYOpmKNb846QiLXaqRSKO7ub44qJ8JTaDZjxy7rIqqK4bZsF45jKiLI5YpVFVQLba4DGra1FpzyI+LYxPZ+IPZCq3bk6d

HdbsHIrnaHTTF2oJKM4DH3ZjHgqvYy6p7q4fZQolLfb+6A5NJKLw4ZEda7StEtQQ6K6nJGFVRI7Y4jJ8Ko6zIbDzIrZLI075FVQE72EbKQ5mLE4EqvJk426XIv6t4rB07s53LvIvJFrgJM5e6s67HppbpFFjJAqw4QrlHPTmRC5p4i7YlS7A5eITCq4FKy5aLxBkmMyEp/KA4IpKIY7UrtTa666LIspwk9ZVSm4gk4xonbIW6jpW6Ha3DiqI6u7s

7+5wFwTW7ome53alJykXSB6iTQBsBwAsTmCDBrj/iQDpD6pQBh5CSR6d6lrhQdq8wWzQGwFwxl4hTSEqTR7mrSRJrmnYh4hGpoBRb7ooxxw8GzQJ7xrl7GRemx4+luY8QcB8RWl/A2lYpd7HZzoLpxw1welgEJp5k6Tp4br5SiTTiMQtiGgGpnAIDihQDsCgjhiRj4AKgejkCZDYTjBMCEAcDKAji6lZCPjPjcDAiThB7YBEBnhoCjkIBB4cCag1

AzlB7CBQBEA8gjmkCTgVmdB2AABWCA2AOQ5Q85cAN4d4D4T4CAwEb4+AH4LYAw9ZjAdoQ4+A/ZnpBYaI6Qh5DZmEiozAUABg+YiATZUYupMwQwV53AN5d5Kk+AoQzo35T5L5IF+AM44As4dAHoCI4QI45Z04QAA=
```
%%