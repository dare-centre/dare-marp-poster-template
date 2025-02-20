# DARE Marp Poster Template

## Setting up Marp
Instructions for using this [Marp](https://marp.app/) template in VSCode:
- Download [Marp extension for VSCode](https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode).
- In VSCode `Preferences->Settings`, search Marp. Enable `Marp: Enable HTML`.
- Add our CSS theme to the list of markdown themes. This can be done by going into `.vscode/settings.json` and adding the css file to the list of Marp themes:

```
{
    ...
    "markdown.marp.themes": [
        "<local-relative-path>/poster.css"
    ]
    ...
}
```
 where `<local-relative-path>` is the path relative to the folder that you have open in VSCode. Alternatively, you can add the path to `Preferences -> Settings` in the field called `Markdown › Marp: Themes`
 For example, if you cloned this repo into a folder in VSCode, it would look like
 ```
 {
    "markdown.marp.themes": [
        "./marp-poster-template/themes/poster.css"
    ],
}
 ```

You can also stick to the template (but this is sneaky and also may break your poster if the template changes).

Ctrl+cmd+P -> Preferences: Open Settings (UI) | search "marp theme" and add item to "Markdown › Marp: Themes" 

```
https://raw.githubusercontent.com/dare-centre/dare-marp-poster-template/main/themes/poster.css
```

## Creating the markdown to generate your poster
- Add the following header to your poster file (`.md`):

```
---
marp: true
theme: poster
paginate: false
size: 36:24
---
```

- You can automatically render your poster file using the preview preview pane with the `Markdown: Open preview` command.
- Note that you can change the `size:` option (this denotes width:height). Available sizes are listed at the top of `./theme/poster.css`; you can also create your own size.

## Exporting the poster 
- The poster can be exported as `pdf`, `jpg`, `png`, and other formats supported by Marp.
- To export, click the Marp icon in the top right corner of the editor and choose `Export slide deck`. ![](./images/marp-export.png)
 