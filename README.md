# Astro's `<Code/>` component `defaultColor` option support demo

Astro version: `4.11.1`

Currently requires changes to files in `node_modules` to make the demo work. I copied the modified files to `node_modules - modified files`, use them to overwrite the files after `npm install`.

Here's the list of `node_module` files I modified:
- `node_modules/astro/components/Code.astro`
- `node_modules/@astrojs/markdown-remark/dist/types.d.ts`
- `node_modules/@astrojs/markdown-remark/dist/shiki.d.ts`
- `node_modules/@astrojs/markdown-remark/dist/shiki.js`



For `Code.astro`, The error message seems to be a false-positive, because the demo runs fine. Not sure how to make it go away though.



## How to view the demo
1. `npm install`
2. Overwrite `node_module` files with the files in `node_module - modified files`
3. `npm run dev`



## References
- [Shiki's `defaultColor` option on Shiki docs](https://shiki.matsu.io/guide/dual-themes#without-default-color)
- [Astro's `<Code/>` component on GitHub](https://github.com/withastro/astro/blob/main/packages/astro/components/Code.astro#L15)
- [Astro's `highlighter.codeToHtml()` on GitHub](https://github.com/withastro/astro/blob/main/packages/markdown/remark/src/shiki.ts#L74)
- [Shiki's `codeToHtml()` on GitHub](https://github.com/shikijs/shiki/blob/main/packages/core/src/code-to-html.ts#L12)
- [Shiki's `CodeToHastOptions` on GitHub](https://github.com/shikijs/shiki/blob/main/packages/core/src/types/options.ts#L117)
