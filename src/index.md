# 🍱 Index

```mermaid
graph TD
    A[Start]
    A --> B[Theory]
    A --> C[Practice]
    B --> D[Design]
    B --> E[Useful]
    C --> F[FAQ]
    C --> G[How to rice thing]
    C --> H[Terminal]
    C --> I[An example ricing journey]
    click D "./out/design.html"
    click E "./out/useful.html"
    click F "./out/faq.html"
    click G "./out/how-to-rice-thing.html"
    click H "./out/terminal.html"
    click I "./out/where-to-start.html"
```

## Credits
Most of the following are members of the r/unixporn discord server.

- Animated Wallpaper - Dazai-san#6969
- Picom Animations - nuxsh#9338
- Uniform Look for GTK & QT Apps, QGtkStyle - Gingka#1796 
- Document has been edited by asdadsdafdfdssfd#7660

I have quoted some people here and there and credited them appropriately

<script type="module">
	import mermaid from 'https://cdn.jsdelivr.net/npm/mermaid@10/dist/mermaid.esm.min.mjs';
	mermaid.initialize({ startOnLoad: false });
    (async () => {
        await mermaid.run({
            querySelector: 'pre[lang="mermaid"] > code'
        })
    })()
</script>
