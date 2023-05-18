<style>
	.cbox-example {
		display: inline-block;
		background: lightcoral;
		color: black;
	}

	.cbox-example *, .cbox-example {
		padding: 1em 1.5em 1.5em 1.5em;
		border: 1px solid;
	}

	.cbox-example > * {
		background: skyblue;
		border: 5px solid black;
	}

	.cbox-example > * > * {
		background: #fafafa;
	}
</style>

# Ricing Terminology
*Some definitons copied word for word from the [Unixporn dictionary](https://www.reddit.com/r/unixporn/wiki/themeing/dictionary/)*

![-](https://upload.wikimedia.org/wikipedia/commons/4/43/Poser.JPG)

## Rice

"Rice" is a word that is commonly used to refer to making visual improvements and customizations on one's desktop. It was inherited from the practice of customizing cheap Asian import cars to make them appear to be faster than they actually were - which was also known as "ricing". Here on /r/unixporn , the word is accepted by the majority of the community and is used sparingly to refer to a visually attractive desktop upgraded beyond the default.

When used as a verb to describe the process of creating a rice, It becomes *ricing*

## Desktop Environment
Desktop Environments, or DEs, have a window manager, along with with panels (think 'Taskbar') and widgets. They also provide a whole range of software. For example, a full installation of Gnome includes everything from configuration utilities to text editors to games. Common DEs include Gnome, KDE, Xfce, and Cinnamon.

## Window Manager
A windows manager or WM, is a tool which adds borders to the windows and allow moving/closing etc with the window. Then they get more complex and add in things like automatic tiling, status bars and widgets. Common WMs include i3 (and it's gaps patch), Openbox, BSPWM, and Awesome.

### Titlebar
This refers to the bar usually above a window's content, that has its title and maybe some action buttons.

![-](../embed/titlebar-eg.png)

## Display Manager
A display manager or DM, is the utility which handles the login screen, usually graphical. Both the [Arch] and [Gentoo] wiki pages have great resources and links to the different display managers. Common display managers are LightDM, G(nome)DM, and SLiM.

## Padding / Margin
This can mean a lot of things in different contexts but usually it refers to something like this

<div class="cbox-example">
	MARGIN
	<div>
		PADDING
		<div>
			CONTENT BOX
		</div>
	</div>
</div>

*Padding* is the extra space between the borders and the content box of the widget.

*Margin* is the space between the border of one box and the border of the another, or the space between 2 entire boxes.

The padding the margin and the content all together make up an entire element.