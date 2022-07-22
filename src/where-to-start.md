# 🥟 A Ricing Roadmap

There is a lot of choice when you start ricing and there are so many things you can dive into that it can easily become overwhelming, So this is a kind of road map I wrote of what things you should do in what order to really understand if you like ricing. Let's begin from the perspective of someone who has recently installed a common distribution (let's go w/ ubuntu or one of its derivatives) and has seen one of the posts on unixporn and wants to also make his desktop look like it.

To have some kind of idea of what our final product will be, Let us aim for something similar to this (w/ the same stuff, style will be different ofc)

![example rice](https://i.redd.it/ge6i053ncpb91.png)

### Necessary Skills
Just like a recipe wont teach you how to boil water, this guide can't explain every little thing either so basic knowledge of ricing terminology is required, Along with the *rare* ability to read documentation and manual pages. Of course the ability to edit and understand basic configuration files is also required. Knowledge of some basic parts of linux will also be extremely helpful (Stuff like hidden directories, file paths, package manager etc).

## 🏃 Escaping The DE
First things first we have the ecosystem of the preinstalled desktop environment to the safe lands of window managers.

Of course you can rice a DE, but most rices are done on a WM so I'll follow that.

I would recommend Bspwm, Openbox & i3 since although being beginner friendly they can be flexible enough to fit most desires, Besides many people are familiar with them and there exist lots of resources for them.

Switching to a WM is as simple as installing the necessary package, hopefully this is as simple as `# $PKGMANAGER install $WM` but if not you'll need to compile the wm from source code, Instructions for doing so should be available in either a COMPILE.md or INSTALL or such.

If you choose i3 or bspwm, You will need to take some time to become familiar with the method of navigating windows by way of keyboard shortcuts and with the tiling layout in general, I'd suggest you take the time to get used to it before continuing on.

* bspwm in particular requires a fair amount of pre requisite knowledge in sh scripting and such. You need sxhkd for defining key bindings.

## Settling Down

### Finding / Creating a color scheme
<!-- NEEDS A LOT OF WORK. -->
This is the foundation the rest of your design will sit upon, The colors you choose can easily make or break a rice, So it is essential to pick a good looking one and build everything around it.

This is largely a matter of personal preference of what / how many colors you choose but generally color schemes have 16 colors with or without foreground and background colors.

Most terminals require 2 shades of white black red cyan magenta yellow blue & green (16 colors in total), One "dim" shade and one "bright" shade, but generally the bright shade just needs to be the same color and distinguishably different from the "dim" shade

I'd also suggest having colors (these can be the same) to represent focus and inactivity and various shades of background colors to visibly identify how high up a UI element is in the z space. (What is more in front of you and what is more behind)

There is also a theming shortcut called ["base16"](https://github.com/chriskempson/base16) which can greatly streamline the ricing process but brings with it its own drawbacks.
<!-- WRITE MORE HERE -->

### Wallpaper

After some time, looking at the plain black default background gets tiring so let's set a pretty background, This may seem like a small step but the background you choose can heavily affect the colors you can use in the rest of your rice. So ideally pick something you can contrast easily and one that isn't visually busy, Your focus shouldn't be immediately attracted to wallpaper at first sight.
* You can find some good places to find wallpapers here: https://nes.is-a.dev/ricing-guide/how-to-rice-thing.html#wallpapers

Especially for minimalist window managers, it is common that they do not include wallpaper setter in which case an external application (usually `feh`) needs to be used.

To illustrate: ![](https://media.discordapp.net/attachments/635625973764849684/998503072781320282/9_-_lmDxmn6.jpg?width=776&height=485) is an example of what I'd call a good wallpaper, it can easily with a color scheme like melange or gruvbox material and there is plenty of contrast to place any desktop widgets if I so choose, of course you have to like it too, its your desktop after all.

## Getting Comfortable

So now we have the very start of a rice, We have chosen a colourscheme and we have a wallpaper to go with it, From here our rice can go whereever you want it to really.

Since we are going to be editing all our configuration files from within our text editor, We should start with ricing that and becoming comfortable in it.

### Editor
I'm writing this with neovim in mind but I'll try to make it as general as possible.
I'll just go through the steps to make your editor to fit in your rice and some extra steps you can take for beautification.

When using neovim with the default colors, this is what we get, Nothing much to look at is it.
![](/embed/editor0.png)

Let's at least start by matching colours with our chosen colourscheme, Depending on whether you made your colourscheme yourself, there will probably already exist a theme made by some poor soul to fit. This becomes less likely on other editors. If you made a base16 theme this isn't really a concern as from how base16 themes work, one can be generated from just the set of colours.

#### Making a theme for VIM (VimScript)
If such a theme doesnt exist, It isnt a big problem since Vim makes it fairly simple to create a theme.  
**Read** `:help highlight` & `:help colorscheme` & `:help coloring`  
Basically every thing with colour in vim belongs to a *highlight group* that specifes things like foreground background & text style. The styles for every highlight group can be modified with the `highlight` command from vimscript

For an example, here is the port of the chocolate theme I made for vim:
```viml
" Typescript
hi TSVariableBuiltin guifg=#d9b27c
hi TSField guifg=#998396
hi TSParameter guifg=#859e82
hi cTSFuncMacro guifg=#d9b27c
hi cStructure guifg=#829e9b
hi cTSConstant guifg=#ab9382
hi TSBoolean guifg=#d08b65
hi cTSKeywordOperator guifg=#829e9bt

" User Interface
hi VertSplit cterm=none gui=none guibg=bg guifg=#302c2b
hi StatusLine guibg=#3d3837 cterm=none gui=none 
hi EndOfBuffer guibg=bg guifg=bg
hi StatusLineNC guibg=#302c2b gui=none cterm=none
```
[[Full File]](https://github.com/undefinedDarkness/rice/blob/master/.config/nvim/colors/chocolate.vim)  
If you spend time configuring extension appearances (Some are astoudingly bad at following default highlight groups) too it can take some time but the basic UI & syntax hl groups shouldn't take too long.

<center>

--- **🚧 This article is still undergoing contruction** ---

</center>