<!-- DUMPING GROUND FOR STUFF FROM HERE AND THERE -->
<!-- TODO: Remove, This should taken care of via git -->

### Parts of a rice

<img class="pxl-art" alt="illustration" src="../embed/ricing-guide.webp" />

### Window Manager Tier list
This is very biased, of course :)
and based on my opinion.
**I HIGHLY RECOMMEND YOU TRY EACH OF THEM AND DECIDE FOR YOURSELF**
Generally, the higher it is up on the list, the more complicated and powerful it is.

| | | | | |
|-|-|-|-|-|
|Best|Awesome| | | |
|Better|XMonad|FVWM|Qtile| |
|Cool|HLWM|Kiwmi|Wayfire| |
|Simple|i3|Openbox|Bspwm|River|
|Unremarkable|leftwm|dwm|2bwm|berry|


If you're new to ricing in general, I'd highly recommend i3 since it's very commonly used, has good documentation, and is a relatively good example of a tiling window manager.
* Use i3-gaps if you're planning to use i3, Sway is pretty much i3-gaps for wayland so you can try that too.
* Sway has not been added because it is basically i3 for wayland and if it were added, it would occupy the same rank.

If you don't want to learn how tiling window managers work (I highly recommend you do), Openbox might be a good choice as it's better than i3 for floating.
You can try iceWM too, which is more fully featured out of the box.
* Awesome might be the best window manager for floating too, overall

If you are just looking for outright power at no expense spared, you're looking at either awesome, xmonad or qtile.
XMonad is very good at moving windows around but it's configured in Haskell, which can be relatively difficult to learn and it has no widget system.
Awesome is good at that too but maybe not to the same extent, but it has an excellent widget system, it's configured in Lua which is relatively easy to learn.
Qtile is similar to awesome, but it uses python and I hear has some serious performance issues, but it has a wayland backend so that might be of note.

[Full List & More details](https://wiki.archlinux.org/title/Window_manager#List_of_window_managers)
[Comparison](https://wiki.archlinux.org/title/Comparison_of_tiling_window_managers)

### Methodology
This "guide" as I call it, isnt that much of a guide but more of a reference, Because *in my opinion* ricing is a very personal thing and such is very hard to teach,
and since its so flexible trying to document every step on your journey that way would be too much work, so I have just collected useful tidbits of knowledge I found
and tried to make it easier to document applications even I found difficult to theme. I have no attempt to hold anyone's hand through ricing through since if I do that
It will become a how-to-make-a-rice-nes-likes guide; And I have a hard time putting such vague ideas about design and color into words, I am not a designer or artist after all.

Along with that, I never meant for this guide to teach you design, That is something best left to professionals

There is however a method to the madness, as you continue you pick up habits and orders in which to do things. Mine (personally) is to just jump right in and worry about the rest later
so I don't really have much to say here but, as an example to follow:

<blockquote>
This is the "framework" I usually follow:
1) Design/Plan how I want my desktop to look like.
2) Search which kind of enviroment I want (wm/de)
  2.1) If DE I go gnome and don't change anything.
  2.2) If WM I do a little bit of research and balance the pros and cons of each wm have to offer to me.
3) Make colorscheme. (iterate it)
4) Tweak WM and search for 3th party tools (bar/terminal/editor)
5) Repeat steps 3 and 4 until I like the result.
My personal preference nowadays is fvwm because is flexible enough for the things I need... the important part imho is iterating it slowly and having fun 

Caelie
</blockquote>
