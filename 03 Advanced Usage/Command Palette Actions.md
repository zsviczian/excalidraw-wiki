---
excalidraw-plugin: parsed
tags:
  - excalidraw
excalidraw-autoexport: svg
excalidraw-open-md: true
excalidraw-export-transparent: true
aliases:
  - WIKI/03+Advanced+Usage/Command+Palette+Actions
permalink: wiki/command-palette
---

# [[Command Palette Actions]]

| Command                                                                                         | Description | Condition when Visible |
| ----------------------------------------------------------------------------------------------- | ----------- | ---------------------- |
| Add back-of-note card                                                                           |             |                        |
| Annotate image in Excalidraw                                                                    |             |                        |
| Convert *.excalidraw to *.md files                                                              |             |                        |
| Convert markdown note to Excalidraw Drawing                                                     |             |                        |
| Convert to file...                                                                              |             |                        |
| Copy ![\[embed link]] for this drawing                                                          |             |                        |
| Copy 'area=' !\[[link]] for selected element to clipboard.                                      |             |                        |
| Copy 'clippedframe=' !\[[link]] for selected element to clipboard.                              |             |                        |
| Copy 'frame=' !\[[link]] for selected element to clipboard.                                     |             |                        |
| Copy 'group=' !\[[link]] for selected element to clipboard.                                     |             |                        |
| Copy [\[link]] for selected element to clipboard.                                               |             |                        |
| Create new drawing - IN A NEW TAB                                                               |             |                        |
| Create new drawing - IN A NEW TAB - and embed into active document                              |             |                        |
| Create new drawing - IN A POPOUT WINDOW                                                         |             |                        |
| Create new drawing - IN A POPOUT WINDOW - and embed into active document                        |             |                        |
| Create new drawing - IN AN ADJACENT WINDOW                                                      |             |                        |
| Create new drawing - IN AN ADJACENT WINDOW - and embed into active document                     |             |                        |
| Create new drawing - IN THE CURRENT ACTIVE WINDOW                                               |             |                        |
| Create new drawing - IN THE CURRENT ACTIVE WINDOW - and embed into active document              |             |                        |
| Crop and mask image                                                                             |             |                        |
| Decompress current Excalidraw file                                                              |             |                        |
| Delete selected image or Markdown file from Obsidian Vault                                      |             |                        |
| Disable autosave until next time Obsidian starts (only set this if you know what you are doing) |             |                        |
| Embed a drawing                                                                                 |             |                        |
| Embed the most recently edited drawing                                                          |             |                        |
| Embeddable Properties                                                                           |             |                        |
| Enable autosave                                                                                 |             |                        |
| Export Image                                                                                    |             |                        |
| Export stencil library as an *.excalidrawlib file                                               |             |                        |
| Frame Settings                                                                                  |             |                        |
| Import an SVG file as Excalidraw strokes (limited SVG support, TEXT currently not supported)    |             |                        |
| Insert active PDF page as image                                                                 |             |                        |
| Insert ANY file                                                                                 |             |                        |
| Insert image or Excalidraw drawing from your vault                                              |             |                        |
| Insert LaTeX formula (e.g. \binom{n}{k} = \frac{n!}{k!(n-k)!}).                                 |             |                        |
| Insert link to file                                                                             |             |                        |
| Insert markdown file from vault                                                                 |             |                        |
| Insert Obsidian Command as a link                                                               |             |                        |
| Insert PDF file from vault                                                                      |             |                        |
| Install or update Excalidraw Scripts                                                            |             |                        |
| Move back-of-note card to File                                                                  |             |                        |
| Obsidian Publish: Find SVG and PNG exports that are out of date                                 |             |                        |
| OCR full drawing re-run: Grab text from freedraw + images to clipboard and doc.props            |             |                        |
| OCR full drawing: Grab text from freedraw + images to clipboard and doc.props                   |             |                        |
| OCR selected elements: Grab text from freedraw + images to clipboard                            |             |                        |
| Open Excalidraw drawing                                                                         |             |                        |
| Open existing drawing - IN A NEW PANE                                                           |             |                        |
| Open existing drawing - IN THE CURRENT ACTIVE PANE                                              |             |                        |
| Open the back-of-the-note of the selected excalidraw image                                      |             |                        |
| Open the image-link or LaTeX-formula editor                                                     |             |                        |
| Read latest release notes                                                                       |             |                        |
| Reset selected image element aspect ratio                                                       |             |                        |
| Save (will also update transclusions)                                                           |             |                        |
| Save image from URL to local file                                                               |             |                        |
| Scale selected embeddable elements to 100% relative to the current canvas zoom                  |             |                        |
| Search for text in drawing                                                                      |             |                        |
| Set selected image element size to 100% of original                                             |             |                        |
| Toggle between Excalidraw and Markdown mode                                                     |             |                        |
| Toggle frame clipping                                                                           |             |                        |
| Toggle frame rendering                                                                          |             |                        |
| Toggle fullscreen mode                                                                          |             |                        |
| Toggle left-handed mode                                                                         |             |                        |
| Toggle property-panel tray-mode                                                                 |             |                        |
| Toggle Text Element between edit RAW and PREVIEW                                                |             |                        |
| Toggle to invert default binding behavior                                                       |             |                        |

The list was generated with this script:
```js
console.log(
  "| Command | Description | Condition when Visible | ID |\n" +
  "| --- | --- | --- | --- |\n" +
  Object.values(app.commands.commands)
    .filter(c=>c.name.startsWith("Excalidraw:") && !c.name.includes(" (Script) "))
    .sort((a,b)=>a.name.toLowerCase().localeCompare(b.name.toLowerCase()))
    .map(c=>`|${c.name}|   |   |${c.id}|`).join("\n")
  )
```


%%
# Excalidraw Data

## Text Elements
## Drawing
```compressed-json
N4KAkARALgngDgUwgLgAQQQDwMYEMA2AlgCYBOuA7hADTgQBuCpAzoQPYB2KqATLZMzYBXUtiRoIACyhQ4zZAHoFAc0JRJQgEYA6bGwC2CgF7N6hbEcK4OCtptbErHALRY8RMpWdx8Q1TdIEfARcZgRmBShcZQUebQB2bQAWGjoghH0EDihmbgBtAF1+CFw4OABlKKhxVFAwSHUMmogiZWlU+oZCBAoAIVxsAGtlUmEOYgBhNnw2Um4IAGIAMRWA

NiWABg7IbBFA7IBJav1K0cGEKZm5iQWARgR7++2IXdJ9qCOM/qGRscnp2bzKDkDjMOC4d7PV7vT76JaEfD4SowYLzQQeKF7LIfY6nNjnADqJHU3D44B2WMOuOB+IQyNREnRJExb2xsIASsI2hxwrk0Ld+BTWVSMgB5cHYNQwbi3DYbQUvSk4jJLThQJa4fQI6VoACsCuhbOOquy5UIRhqPHl5MVwuV+gAKlgoABBVpcCTBABmUBZMOpENdbzYFEk

IWI3A4QkRBqVsIAouMXcHQ+H5hDRlRY3bYcnMw74M1RkJxs9mNhRoiABrcVarACc2h4+pt5cr+AAmtwkvW4i3OkY2AZuHVOvQCEIardyQBfbP+jKckvEHnMPnoYulhUjEhmi2k62dHfESoIODcfuQY8AWTYxAQidwmmCEbQXoIYW3pBIl0BaFHkC9NMr4bsomi4AAFPESTUKg8TxLBtyrAKqAbNouoAJTbJA7IIMo0YQvMpBgZBuoABywas8qoLc

PCrLBaGYRAs4GgCpAAAoEAgMg1ABLzWOOzDfMMm4gXk5KdMC1hghC2LYZAz4DIM8nifUamLKsSSrHRtzyZACy9DwvQbMZemLGRvRkfWZFkWZCwAMw8PZtzOXZtz1u5ty2RJYBFD5qlqfpEzxhMAAiEwTHZ8arNF8a6nZoUuoloX1nZDarPEml2fZST2XlPDMYFfmBRAoZqEggr1AF6nLGsmx2SsSy9EstmVZ0tUtUsKRtfpLWrPZcp2fEEyOYNPn

FWp1XtdFoU8BMuk9YsSz2fG9bxlsi0LCFoU7QtPn6fWmX9aFdlJL0eW3PGhVqRNVX7YsLpLB58StfdCyhcNFm9HZI0uhM9YunZuqhUkZH2fEdk8PGPBJLc33jW1U36fEuq6vWsM/UkLq9PWqx2S6L1IXtgX6fZhmzcTJV3KFRNbAj/lveRzm3JTNWhat9mo/joVUTwrPtXNXkbKlm1IRsEwbCk9OBUjiz1vW7Psz9wVLPGSx2edsV45tUNkfGetu

dBRvXfUt1gLLDlkdj2N2ej4XhUDSwTL0ztuRMuqrB7dkbNDhnw0ViNvXK8vy6doWNerm1yksPAx97ksgydUcbHRdEm75gck4scp1nW2X2RH8cRRF8d5Xl8eeal0uTUHKcTHNbnrI18cuhsrcV8h2u1yZJnp2bFsTEsoXA/Fm3xvE8YupPCW9Ot61pTw8QbEv2UuWD3kBwzWcLNBVtWxr9bu+7tvxATBPZS6SS6lfbmzY59l95nVOg+lItvYfvSf9

9m2rDjIeQ7lXUnM3J8xdLcQG1c7rb0XlpLSQ14y9HiIg06llVhkS7tvW4SQnJOW9mAvmBVIHmyDi6TmwDNq5XtpFUW/17L1gflHXUcM4bewGqFDYJ0iEWxWMZUym0VgfQ+g1J2SQJjdTeqFMicpBo/wltIx+W8qYrCAUA4RLoAZv23isCeE98b1mkRtRmSQDEKJlm9FYJj+EtQ2FI4RxjjF2SkZYt6xiTFcLei6Vu8irGoy5lY5x29UYBKpjwLxY

1N5mO3ljYJNUVjNmbBrJe3i3rNhie1WibiIk1y0UPM6hicmTyEVY8OYiEroKtPkqmqwRqyjplkqBSilhgNUcUtumjGk410ZtdRSR2GVJqtfOi4SbpP1iUsaCMjzFNRdLYqxh0HGbSkfZLxp0Ni3D6aY7JVNPG9MmTkl0zZR5TPiANfp7VUZDLOfpUJLlhmm1Ge1LGfM9mNPKUc7eiDdQVMhkw2pICbF3IzoosZcU+FTJjkUqZIVSmbUkR5F5NVqm

g0Bf3KZExPYMKhcs9pYyQZdI8YdP5m1r72ScZshpYzPEIvagI5FwjmoLLelIoJVzFjGKMiih5+lPHxG+VYiYKN3mNOxtS/SqM6GisWDcuR5LiFRNIUSqZvQvlCpqog+I+jWULGbO5SVdwrQyvGhJW6GBgiZFNDSc4+QfLQBBDJSEbUICKSGCpN6fse6OMstZV62974uX5vpSuXk0paR0rKi2Ws4oJSSklHF7V0qZXEb63K+UfrbRLkQ0qkhyqupy

U1FqwjOpJqUeg05Q0Rp8vBesOpIzgU0pWmtLV21donzrPZJOLjzrOSumPVYs15rhokZ9T+P1ln/UBsSkGYMIY62hrDb+Hinq3BeoO7eYjsa43xoTZC2VyZ81vrTIaqN0a6Xcdvdm9C/EeJ5inANUr5pSLjYGqiEti0DLBizU99S5VUwimrNWGsVoxQwSE/WYHDZJGNpteWisrpnqpnbMK1DGZOxdguzB7tPYgZqj7IyRlspW16DbeDNVemF2TjHO

Oydem9PjqnbD7Vg7/xI+1PK5Ha7F2Q9vOUZdMXcbWR5J92cNi5zxix597H+Ot3bsnImDH9LSN4XR+ukVxOLHHpPaesLZ4+y1dpJeK9NrOVJaSn6Q8R6rqpjjI+qr2qHTPjOt6yyr431FnfXBm1d4zIgd+i2H8v5pT/qHHWgDyFvVouA8Bp10G4yrr5t6E9EHIIoag9BblsH3zwRFgqOtoKaTE/FqJ7akNu3ofQ72TDegsKjmwjheCyHxTU7VQRjm

cliJhRIpxerqlpN6k1D1TWVjqPUcInRPaCW9cWNfSbtUVEP0G9Y2ZUz7Faq63q1xyScmZNrZExpvjbN9ZmyyvVoSZtUvkQt+JB3FiIJm6kzbVMMkPdI2Emt9y619cKa1xpJS33tUkdpbrNS9W0tMgt9hI2rGdPG9vHpGziXYKolqobtxVELaI0tnJ8zVsbGWettZ8PjmuMs5Sw5o2y3Eq+UjyGYCKceMvhshbbzElfJO78vVGSyUUIOX8hbELvsg

oin9/ScLFXbyRVzqFuoweFcafGbFwi8Uw+2YSvVJLJdtYxSTmluTMcdK6jjllqyOXI6aSshbAqr37OMlq8Vmqae3Bld0gm3z0cqsSRqtnuqtUZKdy4hVKLjWVVNU0bIwlfjLmtSVKSoJwQOptc65SXKbscrBeL0NO7FlepstlJy/q3KCeDU1yN12FjBSQ1xqmyVY1pVxom7KKbHKyqzTm5PHVmo+saUsathayJdQaqWvVw1RpvaBbt2JDb569v7X

eraYUW3QaOu2lBF04Oy7ZsO9D2yl0rs2r9cdQMp3g0hnOlhTX1043k4sQVJ6t1kSJrungFMD3IVH6i89HMrdUyZp+7mvNZ+CyPqNziySza5BQqwAbQYKzxhKybSazAYn56wGyixGyQZgFyy9IlZGaEY2zEqoauw0IexexRy+z4ZNZkbNzJwhxCYLDRyxw5a1w0Ydr8b0boEOQFyUG1yiZFzFylxlwVyCZsFISSZUxyhzQNzJzSZapyhybxw9z+w7

ZbI1QaZTwTpvSDzDzDwzxzx6aLzLxarGbrxsHWa6jHyeagzeYnwOYXwual7rI4Lzbr52bOwBYUIxYNiBbUEAINYgKRY+aKEUrtSJZIIC4Cx5ZwIpboJpaiwZYeYkLZZsGUJYEkI+E0JlZ8aiGVbVZBy1acJOF9Ytb0oer8qiLC6LCSIzY9YXb5FLRNIaLCJzajYaZ6JHYbZv5t4rBSJ65jIzYrAraOIGJaptHtEfa1H7b4yvbCJHa6h3aTGXbu7c

4za3bPYCwzErGBoVKcqjG1RfaK55KK4iJlKA56bA4jHj464Q40Eo4tJKqHTK41Rw5q6I5bHnF9YY6m4TKm7Y4DF45DEE4vFKE64HJf4PEM4g7jJ06BJU4na04AmBF9bM7c7PJaqfKVrQLs4+5Whkp85P6hGfbS6m7QplHvRWRi5VJiLYk1E7EK78pa7FKQb3HtTqLxBkkDK5SUkBE/q4p0pWLnb0oG4DFG4UIpw25sErCW6l48ponCqimU4SparS

pwlck67KoJLc7OR6rqr246xMLanhYGqB4BHQBsBwDsTmCDDrgASQDpDmpQDh6iRR5d497T6Cy2zQGwHqHpqV7qQx72pySZo2nYh4hWpoAWw34YzJzcGLSJ5poV5mS+lx7+nfr8QcCCT2l/COljLd71TdI76d44Z1wSGelxk/wZ5fo3QSQzgsQ2iGgWpnAIDihQDsCgiRjRj4AKhejkCZC4TjBMCEAcDKAjgSQYAcBPgvjcDAiTjB7YBEDnhoCTkI

DB6jmZATmkBTnDnCBQBEA8irmTjVmdB2AABWCA2AOQ5Qo5cAt494j4z4CAIE74+An4NoAwTZjADoQ4+AQ5PphYaI6Qp5zZ2EiozAUABgBYiArZMYw5MwQwd53AD5T56k+AoQro/5b5H5EF+As44Ac4dAXoCI4QI4VZM4QAA=
```
%%