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
Excalidraw adds a number of command palette actions to Obsidian. Most of these commands are context sensitive. Some only work in markdown editor, other in Excalidraw. Some only if certain type of elements or lines in markdown are selected e.g.: only if an image is selected, or only if the cursor is on an eligible line, for example a line that contains a link to an image or a pdf document `![[image.svg]]`


| Command                                                                                                     | Description | Condition when Visible | ID                                                                         |
| ----------------------------------------------------------------------------------------------------------- | ----------- | ---------------------- | -------------------------------------------------------------------------- |
| Excalidraw: Add back-of-note card                                                                           |             |                        | obsidian-excalidraw-plugin:universal-card                                  |
| Excalidraw: Annotate image in Excalidraw                                                                    |             |                        | obsidian-excalidraw-plugin:annotate-image                                  |
| Excalidraw: Convert `*.excalidraw` to `*.md` files                                                          |             |                        | obsidian-excalidraw-plugin:convert-excalidraw                              |
| Excalidraw: Convert markdown note to Excalidraw Drawing                                                     |             |                        | obsidian-excalidraw-plugin:convert-to-excalidraw                           |
| Excalidraw: Convert to file...                                                                              |             |                        | obsidian-excalidraw-plugin:convert-text2MD                                 |
| Excalidraw: Copy `![[embed link]] for this drawing`                                                         |             |                        | obsidian-excalidraw-plugin:copy-link-to-drawing                            |
| Excalidraw: Copy 'area=' `![[link]] for selected element to clipboard.`                                     |             |                        | obsidian-excalidraw-plugin:insert-link-to-element-area                     |
| Excalidraw: Copy 'clippedframe=' `![[link]] for selected element to clipboard.`                             |             |                        | obsidian-excalidraw-plugin:insert-link-to-element-frame-clipped            |
| Excalidraw: Copy 'frame=' `![[link]] for selected element to clipboard.`                                    |             |                        | obsidian-excalidraw-plugin:insert-link-to-element-frame                    |
| Excalidraw: Copy 'group=' `![[link]] for selected element to clipboard.`                                    |             |                        | obsidian-excalidraw-plugin:insert-link-to-element-group                    |
| Excalidraw: Copy `[[link]]` for selected element to clipboard.                                              |             |                        | obsidian-excalidraw-plugin:insert-link-to-element                          |
| Excalidraw: Create new drawing - IN A NEW TAB                                                               |             |                        | obsidian-excalidraw-plugin:excalidraw-autocreate-newtab                    |
| Excalidraw: Create new drawing - IN A NEW TAB - and embed into active document                              |             |                        | obsidian-excalidraw-plugin:excalidraw-autocreate-and-embed-new-tab         |
| Excalidraw: Create new drawing - IN A POPOUT WINDOW                                                         |             |                        | obsidian-excalidraw-plugin:excalidraw-autocreate-popout                    |
| Excalidraw: Create new drawing - IN A POPOUT WINDOW - and embed into active document                        |             |                        | obsidian-excalidraw-plugin:excalidraw-autocreate-and-embed-popout          |
| Excalidraw: Create new drawing - IN AN ADJACENT WINDOW                                                      |             |                        | obsidian-excalidraw-plugin:excalidraw-autocreate                           |
| Excalidraw: Create new drawing - IN AN ADJACENT WINDOW - and embed into active document                     |             |                        | obsidian-excalidraw-plugin:excalidraw-autocreate-and-embed                 |
| Excalidraw: Create new drawing - IN THE CURRENT ACTIVE WINDOW                                               |             |                        | obsidian-excalidraw-plugin:excalidraw-autocreate-on-current                |
| Excalidraw: Create new drawing - IN THE CURRENT ACTIVE WINDOW - and embed into active document              |             |                        | obsidian-excalidraw-plugin:excalidraw-autocreate-and-embed-on-current      |
| Excalidraw: Crop and mask image                                                                             |             |                        | obsidian-excalidraw-plugin:crop-image                                      |
| Excalidraw: Decompress current Excalidraw file                                                              |             |                        | obsidian-excalidraw-plugin:excalidraw-unzip-file                           |
| Excalidraw: Delete selected image or Markdown file from Obsidian Vault                                      |             |                        | obsidian-excalidraw-plugin:delete-file                                     |
| Excalidraw: Disable autosave until next time Obsidian starts (only set this if you know what you are doing) |             |                        | obsidian-excalidraw-plugin:excalidraw-disable-autosave                     |
| Excalidraw: Duplicate selected image with a different image ID                                              |             |                        | obsidian-excalidraw-plugin:duplicate-image                                 |
| Excalidraw: Embed a drawing                                                                                 |             |                        | obsidian-excalidraw-plugin:excalidraw-insert-transclusion                  |
| Excalidraw: Embed the most recently edited drawing                                                          |             |                        | obsidian-excalidraw-plugin:excalidraw-insert-last-active-transclusion      |
| Excalidraw: Embeddable Properties                                                                           |             |                        | obsidian-excalidraw-plugin:excalidraw-embeddable-poroperties               |
| Excalidraw: Enable autosave                                                                                 |             |                        | obsidian-excalidraw-plugin:excalidraw-enable-autosave                      |
| Excalidraw: Export Image                                                                                    |             |                        | obsidian-excalidraw-plugin:export-image                                    |
| Excalidraw: Export stencil library as an *.excalidrawlib file                                               |             |                        | obsidian-excalidraw-plugin:excalidraw-download-lib                         |
| Excalidraw: Frame Settings                                                                                  |             |                        | obsidian-excalidraw-plugin:frame-settings                                  |
| Excalidraw: Import an SVG file as Excalidraw strokes (limited SVG support, TEXT currently not supported)    |             |                        | obsidian-excalidraw-plugin:import-svg                                      |
| Excalidraw: Insert active PDF page as image                                                                 |             |                        | obsidian-excalidraw-plugin:insert-active-pdfpage                           |
| Excalidraw: Insert ANY file                                                                                 |             |                        | obsidian-excalidraw-plugin:universal-add-file                              |
| Excalidraw: Insert image or Excalidraw drawing from your vault                                              |             |                        | obsidian-excalidraw-plugin:insert-image                                    |
| Excalidraw: Insert last active PDF page as image                                                            |             |                        | obsidian-excalidraw-plugin:insert-pdf                                      |
| Excalidraw: Insert LaTeX formula (e.g. \binom{n}{k} = \frac{n!}{k!(n-k)!}).                                 |             |                        | obsidian-excalidraw-plugin:insert-LaTeX-symbol                             |
| Excalidraw: Insert link to file                                                                             |             |                        | obsidian-excalidraw-plugin:insert-link                                     |
| Excalidraw: Insert markdown file from vault                                                                 |             |                        | obsidian-excalidraw-plugin:insert-md                                       |
| Excalidraw: Insert Obsidian Command as a link                                                               |             |                        | obsidian-excalidraw-plugin:insert-command                                  |
| Excalidraw: Install or update Excalidraw Scripts                                                            |             |                        | obsidian-excalidraw-plugin:scriptengine-store                              |
| Excalidraw: Move back-of-note card to File                                                                  |             |                        | obsidian-excalidraw-plugin:convert-card-to-file                            |
| Excalidraw: Obsidian Publish: Find SVG and PNG exports that are out of date                                 |             |                        | obsidian-excalidraw-plugin:excalidraw-publish-svg-check                    |
| Excalidraw: OCR full drawing re-run: Grab text from freedraw + images to clipboard and doc.props            |             |                        | obsidian-excalidraw-plugin:rerun-ocr                                       |
| Excalidraw: OCR full drawing: Grab text from freedraw + images to clipboard and doc.props                   |             |                        | obsidian-excalidraw-plugin:run-ocr                                         |
| Excalidraw: OCR selected elements: Grab text from freedraw + images to clipboard                            |             |                        | obsidian-excalidraw-plugin:run-ocr-selectedelements                        |
| Excalidraw: Open Excalidraw drawing                                                                         |             |                        | obsidian-excalidraw-plugin:open-image-excalidraw-source                    |
| Excalidraw: Open existing drawing - IN A NEW PANE                                                           |             |                        | obsidian-excalidraw-plugin:excalidraw-open                                 |
| Excalidraw: Open existing drawing - IN THE CURRENT ACTIVE PANE                                              |             |                        | obsidian-excalidraw-plugin:excalidraw-open-on-current                      |
| Excalidraw: Open the back-of-the-note of the selected excalidraw image                                      |             |                        | obsidian-excalidraw-plugin:flip-image                                      |
| Excalidraw: Open the image-link or LaTeX-formula editor                                                     |             |                        | obsidian-excalidraw-plugin:open-link-props                                 |
| Excalidraw: Read latest release notes                                                                       |             |                        | obsidian-excalidraw-plugin:release-notes                                   |
| Excalidraw: Reset selected image element aspect ratio                                                       |             |                        | obsidian-excalidraw-plugin:reset-image-ar                                  |
| Excalidraw: Save (will also update transclusions)                                                           |             |                        | obsidian-excalidraw-plugin:save                                            |
| Excalidraw: Save image from URL to local file                                                               |             |                        | obsidian-excalidraw-plugin:excalidraw-convert-image-from-url-to-local-file |
| Excalidraw: Scale selected embeddable elements to 100% relative to the current canvas zoom                  |             |                        | obsidian-excalidraw-plugin:excalidraw-embeddables-relative-scale           |
| Excalidraw: Search for text in drawing                                                                      |             |                        | obsidian-excalidraw-plugin:search-text                                     |
| Excalidraw: Set selected image element size to 100% of original                                             |             |                        | obsidian-excalidraw-plugin:reset-image-to-100                              |
| Excalidraw: Toggle between Excalidraw and Markdown mode                                                     |             |                        | obsidian-excalidraw-plugin:toggle-excalidraw-view                          |
| Excalidraw: Toggle frame clipping                                                                           |             |                        | obsidian-excalidraw-plugin:disable-frameclipping                           |
| Excalidraw: Toggle frame rendering                                                                          |             |                        | obsidian-excalidraw-plugin:disable-framerendering                          |
| Excalidraw: Toggle fullscreen mode                                                                          |             |                        | obsidian-excalidraw-plugin:fullscreen                                      |
| Excalidraw: Toggle left-handed mode                                                                         |             |                        | obsidian-excalidraw-plugin:toggle-lefthanded-mode                          |
| Excalidraw: Toggle property-panel tray-mode                                                                 |             |                        | obsidian-excalidraw-plugin:tray-mode                                       |
| Excalidraw: Toggle Text Element between edit RAW and PREVIEW                                                |             |                        | obsidian-excalidraw-plugin:toggle-lock                                     |
| Excalidraw: Toggle to invert default binding behavior                                                       |             |                        | obsidian-excalidraw-plugin:disable-binding                                 |


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