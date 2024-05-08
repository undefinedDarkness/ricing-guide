# Comparison of terminals

<table>
<colgroup>
<col  class="org-left">
<col  class="org-left">
<col  class="org-left">
<col  class="org-left">
<col  class="org-left">
<col  class="org-left">
<col  class="org-left">
<col  class="org-left">
<col  class="org-left">
<col  class="org-left">
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">Name</th>
<th scope="col" class="org-left">Ligatures</th>
<th scope="col" class="org-left">Fallback</th>
<th scope="col" class="org-left">Advanced</th>
<th scope="col" class="org-left">Bitmaps</th>
<th scope="col" class="org-left">Wayland</th>
<th scope="col" class="org-left">Tabs</th>
<th scope="col" class="org-left">Images</th>
<th scope="col" class="org-left">Config</th>
<th scope="col" class="org-left">Rating</th>
</tr>
</thead>
<tbody>
<tr>
<td class="org-left">Wezterm</td>
<td class="org-left">Y</td>
<td class="org-left">Y</td>
<td class="org-left">Y</td>
<td class="org-left">Y</td>
<td class="org-left">Y</td>
<td class="org-left">Y</td>
<td class="org-left">Y</td>
<td class="org-left">Lua</td>
<td class="org-left">10/10</td>
</tr>
<tr>
<td class="org-left">Alacritty</td>
<td class="org-left">P</td>
<td class="org-left">N</td>
<td class="org-left">N</td>
<td class="org-left">Y</td>
<td class="org-left">Y</td>
<td class="org-left">N</td>
<td class="org-left">N</td>
<td class="org-left">Yaml</td>
<td class="org-left">5/10</td>
</tr>
<tr>
<td class="org-left">Kitty</td>
<td class="org-left">Y</td>
<td class="org-left">N</td>
<td class="org-left">Y</td>
<td class="org-left">N</td>
<td class="org-left">Y</td>
<td class="org-left">Y</td>
<td class="org-left">Y</td>
<td class="org-left">Custom</td>
<td class="org-left">8/10</td>
</tr>
<tr>
<td class="org-left">Xterm</td>
<td class="org-left">N</td>
<td class="org-left">N</td>
<td class="org-left">N</td>
<td class="org-left">Y</td>
<td class="org-left">N</td>
<td class="org-left">N</td>
<td class="org-left">Y</td>
<td class="org-left">Xresources</td>
<td class="org-left">7/10</td>
</tr>
<tr>
<td class="org-left">St</td>
<td class="org-left">P</td>
<td class="org-left">P</td>
<td class="org-left">N</td>
<td class="org-left">Y</td>
<td class="org-left">N</td>
<td class="org-left">N</td>
<td class="org-left">P</td>
<td class="org-left">C header</td>
<td class="org-left">7/10</td>
</tr>
<tr>
<td class="org-left">Foot</td>
<td class="org-left">N</td>
<td class="org-left">Y</td>
<td class="org-left">N</td>
<td class="org-left">Y</td>
<td class="org-left">Y</td>
<td class="org-left">N</td>
<td class="org-left">Y</td>
<td class="org-left">INI</td>
<td class="org-left">7/10</td>
</tr>
<tr>
<td class="org-left">Vte</td>
<td class="org-left">N</td>
<td class="org-left">N</td>
<td class="org-left">N</td>
<td class="org-left">N</td>
<td class="org-left">N</td>
<td class="org-left">N</td>
<td class="org-left">P</td>
<td class="org-left">GUI</td>
<td class="org-left">5/10</td>
</tr>
</tbody>
</table>

**Notes:**   

-   *Fallback* refers to the ability to fallback fonts, that is find a character in the next font in a list if it is not in the first one.
-   *Advanced* refers to the capability of advanced open type features, primarily stylistic sets
-   The foot terminal is wayland exclusive
-   If you're thinking about using st, I highly suggest you use [st-flexipatch](https://github.com/bakkeby/st-flexipatch) right from the start, It will save you a lot of time
-   VTE refers to any terminal that uses the [vte](https://gitlab.gnome.org/GNOME/vte) library as a shortcut, this does almost 99.99% of the heavy lifting for you so behaviour across different vte terminals tends to be the same, for example, gnome-terminal, xfce-terminal, [tym](https://github.com/endaaman/tym) all leverage the vte library.

[Fork for ligatures in alacritty](https://github.com/zenixls2/alacritty) - Even the alacritty author recommends you simply use another terminal if you want ligatures.  
It is possible to enable bitmap fonts in kitty, using the `kitty-bitmap` AUR package, [More instructions](https://github.com/slavfox/Cozette#kitty) - The author does not and will never support bitmap fonts  - *I havent got this to work personally but ymmv*

Issue page for sixel support in VTE: <https://gitlab.gnome.org/GNOME/vte/-/issues/253>  

[Arch Wiki Page](https://wiki.archlinux.org/title/List_of_applications#Terminal)  


# Images in the terminal

This is an often sought after feature and often used with fetch scripts.  
Right now there is no standard and each terminal does their own thing, more and more are supporting [Sixel](https://en.wikipedia.org/wiki/Sixel), though, so maybe that will end up being the standard.  
For terminals without image support entirely, there are hacks using `w3m-img` and `uberzerg` to get them&#x2026;but they're finicky and don't just work™, so I'd recommend against them.  
[Full article](https://github.com/dylanaraps/neofetch/wiki/Images-in-the-terminal)  

XTerm (compiled with &#x2013;enable-sixel-graphics option) does support sixel,  
You should launch xterm with “-ti vt340” option. The SIXEL palette is limited to a maximum of 16 colors. To avoid this limitation, Try  

**Overview:**  
Alacritty doesn't support images and needs a hack;  
Wezterm natively supports iterms2's image format & sixel;  
Kitty has its own format;  
Foot supports sixel;  
Xterm supports sixel;  
St can support sixel via a [patch](https://gitlab.com/exorcist365/dotfulls/-/blob/master/.local/share/src/st/patches/0001-add-st-sixel.patch)  


# Prompts

A shell is usually configured with a *prompt*. This is a small indicator to tell you the computer is waiting for user input, Its usually printed on every new line after the end of a command in a shell  
Eg:  

    $ uname -r
    5.10.11-11-amd64
    $ neofetch

In this example, `$` is the prompt character.  
You can make it very fancy and make it display some useful information if you so like.  

[Default Format Specifiers](https://www.gnu.org/software/bash/manual/html_node/Controlling-the-Prompt.html) (for Bash)  
of note:  
`\[` and `\]` are used to denote characters that must not be printed (color escape codes for example), make sure to use them or the prompt calculation will be wrong.  

If you'd rather just not bother doing it yourself, You can use [Starship](https://starship.rs/) to get a pre-made one, rtfm manual for how to modify it.  

Example prompt (this is gentoo's default one):  
`PS1='\[\033[01;31m\]\h\[\033[01;34m\] \W \$\[\033[00m\] '`  


## Terminal Color Codes & Decorations

Terminals generally support a couple or more of 3 color modes, they are:  

-   24 Bit Colour True Color (Full RGB Color)
-   256 Color
-   8 Color (Everything supports this one)

**The reset code is `\033[0m`** (This removes any formatting)  
\*This is how you change text formatting in the terminal by putting these codes in between the text you want to be formatted.  

To change foreground color:  
`\033[3<N>m`  

To change background color:  
`\033[4<N>m`  

To change foreground color to bright:  
`\033[3<N>;1m`  

To change background color to bright:  
`\033[4<N>;1m`  

Where &lt;N&gt; is one of the following:  

<table>
<colgroup>
<col  class="org-left">
<col  class="org-right">
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">Color</th>
<th scope="col" class="org-right">Number</th>
</tr>
</thead>
<tbody>
<tr>
<td class="org-left">Black</td>
<td class="org-right">0</td>
</tr>
<tr>
<td class="org-left">Red</td>
<td class="org-right">1</td>
</tr>
<tr>
<td class="org-left">Green</td>
<td class="org-right">2</td>
</tr>
<tr>
<td class="org-left">Yellow</td>
<td class="org-right">3</td>
</tr>
<tr>
<td class="org-left">Blue</td>
<td class="org-right">4</td>
</tr>
<tr>
<td class="org-left">Magenta</td>
<td class="org-right">5</td>
</tr>
<tr>
<td class="org-left">Cyan</td>
<td class="org-right">6</td>
</tr>
<tr>
<td class="org-left">White</td>
<td class="org-right">7</td>
</tr>
</tbody>
</table>

### Decorations

-   Bold `\033[1m`
-   Italic `\033[3m`
-   Underline `\033[4m`
-   Reversed `\033[7m`
