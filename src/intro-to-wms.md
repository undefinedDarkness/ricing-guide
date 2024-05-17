<style>
	.floating-demo {
		display: inline-flex; 
		box-shadow: 20px 10px 0;
	}
	.tiling-demo *, .floating-demo {
		margin: 1em 0 2em 0; 
		padding: 2em;
	}
	.tiling-demo, .tiling-demo *, .floating-demo {
		border: 1px solid;
	}
</style>
# An Introduction to Window Managers
Generally when creating a rice, we want the most control and customizability at our fingertips.

Desktop Environments while perfectly usable for most purposes, make extensive customization more troublesome than necessary. To avoid this trouble we have a bare bones window manager which does not undertake any more responsibility than managing your windows (some do more than this but its not important right now). We're now given the responsibility of making our desktop perfectly suited to our needs exactly like how we want it.

For starting out, I'd recommend one of i3, bspwm and openbox to begin with, they have a lot of community support and openbox in particular should be familiar in function to most, while i3 serves as a nice introduction to tiling window managers in general.

# Getting used to a Window Manager

## Mode

Window managers are largely divided into 2 varieties based on how they function, There are *stacking* window managers and *tiling* window managers

### Stacking / Floating

<div class="floating-demo">
	I am a window and I can be moved and resized freely
</div>

These work exactly like you'd expect in MacOS or Windows where windows can be freely moved and resized, Even moved outside the screen edges.

Usually windows are accompanied with titlebars with a window title or action buttons.

I won't go into much detail about these since if you've used a computer before, You're familiar with how they work.

### Tiling

<table class="tiling-demo">
<tr>
	<td rowspan="2">
		Master
	</td>
	<td>
		Child 1
	</td>
</tr>
<tr>
	<td>Child 2</td>
</tr>
</table>

Above is just an example of how windows are placed in tiling window layout.

When they're tiled, windows have no control of how much size they occupy, and they cannot be freely be moved, their position is dictated by the layout.

This manner may seem restrictive at first but not having to spend time figuring out window positions manually and moving windows like a wizard with keybinds helps greatly with productivity.

By manner of how it works, Complex rules can be setup for the position of a window so it can be fine tweaked to a great extent.

There are many dozens of different tiling layouts with each window manager usually only using a few.

**Read the documentation for your chosen wm and see if you can understand it.**

There are many tiling window managers but I'd recommend i3 to start with.

Consult this if you'd like more choice: https://wiki.archlinux.org/title/Comparison_of_tiling_window_managers

For an example of the kinds of layouts possible with a tiling window manager, see the [FrakenWM manual page](https://raw.githubusercontent.com/sulami/frankenwm/master/frankenwm.1)

## Usage
All WM's are designed especially to be used entirely from the keyboard. They can also use mouse controls but this mostly applies to floating window managers.

They all have their own default keybinds so it'll depend on which one you choose.

There isnt really any good way to get used to this, It only comes with practice.