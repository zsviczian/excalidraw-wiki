---
excalidraw-plugin: parsed
excalidraw-onload-script: "FILENAME_FILTER=/^icon -/i;KEYWORD_GRABBER=/(?:icon -)?([^-]*)-?/i;COLS=10;HEIGHT=180;WIDTH=180;TEXTHEIGHT=40;PADDING=50;const api = ea.getExcalidrawAPI();const f=ea.targetView.file;icons=app.vault.getFiles().filter(f=>(f.extension!=='md'||ea.isExcalidrawFile(f))&&f.basename.toLowerCase().match(FILENAME_FILTER)).sort((a,b)=>a.basename.toLowerCase()<b.basename.toLowerCase()?-1:1);const { zenModeEnabled, linkOpacity, trayModeEnabled, penMode, penDetected, allowPinchZoom, allowWheelZoom, pinnedScripts, customPens} = api.getAppState();api.resetScene();api.updateScene({appState: { zenModeEnabled, linkOpacity, trayModeEnabled, penMode, penDetected, allowPinchZoom, allowWheelZoom, pinnedScripts, customPens}});col=0;row=0;for(icon of icons) { id=await ea.addImage(col*(WIDTH+PADDING),row*(HEIGHT+PADDING+TEXTHEIGHT),icon); if(f!==ea.targetView.file && ea.targetView?.getViewType?.()!=='excalidraw') return; if(!id) continue; keywords=icon.basename.match(KEYWORD_GRABBER)[1].trim(); ea.style.verticalAlign='top'; ea.style.textAlign='center'; ea.style.fontSize=12; el=ea.getElement(id); ratio=el.width/WIDTH; if(el.height/ratio>HEIGHT) ratio=el.height/HEIGHT; el.width=el.width/ratio; el.height=el.height/ratio; el.locked = true; ea.style.strokeColor='black'; labelID=ea.addText(col*(WIDTH+PADDING)-PADDING/2+10,row*(HEIGHT+PADDING+TEXTHEIGHT)+HEIGHT+PADDING/2-10,keywords,{ width:WIDTH+PADDING-20, height:TEXTHEIGHT-20, textAlign:'center', textVerticalAlign:'top', autoResize: false, }); ea.getElement(labelID).locked = true; if(++col===COLS) { row++; col=0; await ea.addElementsToView(false,false,false); ea.targetView.clearDirty(); ea.clear(); }}await ea.addElementsToView(false,false,false);ea.targetView.clearDirty();api.zoomToFit();api.updateContainerSize(ea.getViewElements().filter(el=>el.type==='rectangle'));"
---
#exclude 

# Excalidraw Data
## Text Elements
%%
## Drawing
```compressed-json
N4KAkARALgngDgUwgLgAQQQDwMYEMA2AlgCYBOuA7hADTgQBuCpAzoQPYB2KqATLZMzYBXUtiRoIACyhQ4zZAHoFAc0JRJQgEYA6bGwC2CgF7N6hbEcK4OCtptbErHALRY8RMpWdx8Q1TdIEfARcZgRmBShcZQUebQAWbQAGGjoghH0EDihmbgBtAF1+CFw4OABlKKhxVFAwSHUMmogiZWlU+oZCBAoAIVxsAGtlUmEOYgBhNnw2Um4IAGIAMxXV

jshsEUDsgElq/UrRwYQpmbmJBYBGBGvr9YhN0m2oPYz+oZGxyenZ+ahyDjMOC4Z73R7PV76ABihHw+EqMGC80EHjBWyyL32hzYxwA6iR1Nw+OANujdlj/jiEAikRIUSQ0U8MZCAErCNoccK5NCXfikpnkjIAeWB2DUMG4lySST5DzJmIyUM4UChuH0sIlaAArLLwcz9krsuVCEYajwZSS5QKFfoACpYKAAQVaXAkwSWUEZEIpIKdTzYFEkIWI3A4

QjhuvlkIAouNHf7A8H5iDRlRI9bIfHU7b4M1RkJxvdmNhRnCABrcABs1e0AHYdZbi6X8ABNKsATkSDc6RjYBm4dU69AIQhqlxJAF9096MmyC8ROcxueh84XZSMSMbTUSLZ0N8RKgg4Nxu5B9wBZNjEBCx3CaYIhtBLAhhdekEinX5oQeQXrTR/oAsEztsBwHrJALIIMo4YgvMCzRgAIohiEQJO04YtixwilA7CAqG4b4LKSzkJkkHjEwhAcMoA4k

pAWR3g+3D/KOfIbEQx5oMxCCsRAHBqjUXE8cIUBEJyTGkKOaGWnYABWCDYDk5R8XAl7Xre94IABz74K+loDDhjC2n2+A0fUDS5si6QKbh4FyswUAGDmiD4RGtEtGwQyadw2m6WZLShE61mGcZLn4JO4BTnQSywuEA4TiAE5AA===
```
%%