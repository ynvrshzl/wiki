---
description: This button will authorize a github commit.
---

```dataviewjs 
// low level program data
const { shell } = require("electron");
const self = dv.current();

const create = {
	button: function(properties){ 
	
		const button = dv.el("button"); 
		button.classList.add(properties.classes); 
		button.innerHTML = properties.text; 
		button.style.margin = "5px";
		button.onclick = properties.onclick ?? undefined; 
	}
}
const buttons =  [
	{
		text: "Commit", 
		classes: "mod-cta", 
		onclick: () => { 
			new Notice("Awaiting functional git implementation, inside obsidian!")
		}
	},
	{
		text: "Open in GitHub", 
		onclick: () => { 
			new Notice("Awaiting functional git implementation, inside obsidian!"),
			shell.openExternal("https://github.com/ynvrshzl"); 
		}
	},
	{
		text: "Open vault in system",
		onclick: () => { 
			new Notice(`Opening vault as system folder..." `);
			shell.openExternal(self.extern); 
		}
	},
]
buttons.forEach((btn) => create.button(btn));
```
