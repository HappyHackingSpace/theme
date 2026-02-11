# @happyhackingspace/meta

React component for generating Open Graph/etc meta tags for Happy Hacking Space pages.
Designed for Next.js but framework-agnostic.

Not recommended for non-Happy Hacking Space sites—you’ll get Happy Hacking Space favicons :)

## Usage

```bash
yarn add @happyhackingspace/meta
# npm i @happyhackingspace/meta
```

Example for [hackathons.happyhacking.space](https://hackathons.happyhacking.space):

```js
// import Head from 'next/head'

<Meta
  as={Head} // component to wrap tags in, defaults to React.Fragment
  name="Happy Hacking Space" // site name
  title="Hackathons" // page title
  description="List of upcoming high school hackathons" // page description
  image="https://hackathons.happyhacking.space/card.png" // large summary image URL
  color="#ec3750" // theme color
  manifest="/site.webmanifest" // link to site manifest
/>
```

All props are optional. If you include multiple times, the tags from the last
instance will be used.

MIT License
