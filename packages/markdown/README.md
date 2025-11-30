# `@happyhackingspace/markdown`

Render Markdown to HTML, Happy Hacking Space-style. Used primarily on the [Happy Hacking Space Workshops](https://happyhackingspace.dev/workshops/) site.

```sh
yarn add @happyhackingspace/markdown
# npm i @happyhackingspace/markdown
```

[**Try the demo**](https://markdown.happyhackingspace.dev)

## Usage

This package does not include any frontend code, such as React or CSS.

This package is designed for rendering at build or otherwise on a server, not client-side—
the bundle size is significant & it’s not been optimized for performance.

Always use with `await`.

```js
import fs from 'fs'
import md from '@happyhackingspace/markdown'

const getReadme = async () => (
  const text = fs.readFileSync('./README.md', 'utf8')
  return await md(text, '/README.md', '/static')
)
```

| Param       | Default        | Description                                                     |
| ----------- | -------------- | --------------------------------------------------------------- |
| input       | Req’d!         | String. The Markdown text to transform.                         |
| filePath    | `'/README.md'` | String. The Markdown’s path (for fixing relative image links).  |
| imagePrefix | `'/'`          | String. A prefix for the path to relative images.               |
| removeTitle | `false`        | Bool. Remove starting `h1` (if titles are rendered separately). |

If you need to parse frontmatter, we recommend using [gray-matter](https://npm.im/gray-matter)
alongside `@happyhackingspace/markdown`, but it's not included in this package.

***

Partially based on the [Next.js documentation site](https://github.com/zeit/next-site/pull/473/files#diff-879732a0915babd1688248ad1144c2d4).

MIT License
