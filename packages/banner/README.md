# @happyhackingspace/banner

Add a Happy Hacking Space banner to your React website.

## Installation

```bash
npm install @happyhackingspace/banner
# or
yarn add @happyhackingspace/banner
```

## Usage

```jsx
import Banner from '@happyhackingspace/banner'

export default () => (
  <div>
    <Banner />
    <h1>Your awesome site</h1>
  </div>
)
```

### Props

- `year` - Select a banner year (2016-2024). Defaults to current year.
- `style` - Customize inline styles for the banner image.
- Any other props are passed to the underlying `<a>` element.

```jsx
<Banner year={2023} style={{ width: '180px' }} />
```

## License

MIT License
