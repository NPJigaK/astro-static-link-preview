# astro-static-link-preview

[![npm version](https://img.shields.io/npm/v/astro-static-link-preview.svg)](https://www.npmjs.com/package/astro-static-link-preview) 
[![npm downloads](https://img.shields.io/npm/dt/astro-static-link-preview.svg)](https://www.npmjs.com/package/astro-static-link-preview) 
[![license](https://img.shields.io/npm/l/astro-static-link-preview.svg)](https://github.com/NPJigaK/astro-static-link-preview/blob/main/LICENSE)  

A **zero-dependency** Astro component that renders social-style link-preview cards *statically* at build time.  
Choose from six built-in themes (`default`, `small`, `facebook`, `x`, `linkedin`, `discord`) or roll your own with CSS variables.

---

## Features

|  |  |
|---|---|
| **Static rendering** | No client-side fetches — perfect for blogs, docs & MDX content. |
| **Six ready-made themes** | Recreate the look of Facebook, X (Twitter), LinkedIn, Discord, etc. |
| **Automatic favicon** | `default` & `small` use Google Favicon API for the publisher logo. |
| **Graceful fall-back** | Missing image? A built-in SVG placeholder scales to any card size. |
| **Type-safe** | Exports an interface for all props. |
| **Pure CSS** | No external style sheets or JS bundles. |
---

## install
```bash
# choose one
npm install astro-static-link-preview
yarn add astro-static-link-preview
pnpm add astro-static-link-preview
```

## Usage
### import
`.astro`
```astro
---
import { LinkPreview } from "astro-static-link-preview";
---
```

`.mdx`
```mdx
import { LinkPreview } from "astro-static-link-preview";
```

### Drop in a component
```mdx
<LinkPreview
  url="https://astro.build"
  title="Astro Homepage"
  description="Astro builds fast content sites, powerful web applications, dynamic server APIs, and everything in-between."
  image="https://astro.build/og/astro.jpg"
/>
```
![default](doc/default.jpg)

```mdx
<LinkPreview
  url="https://astro.build"
  title="Astro Homepage"
  description="Astro builds fast content sites, powerful web applications, dynamic server APIs, and everything in-between."
  image="https://astro.build/og/astro.jpg"
  theme="small"
/>
```
![small](doc/small.jpg)

```mdx
<LinkPreview
  url="https://astro.build"
  title="Astro Homepage"
  description="Astro builds fast content sites, powerful web applications, dynamic server APIs, and everything in-between."
  image="https://astro.build/og/astro.jpg"
  theme="facebook"
/>
```
![facebook](doc/facebook.jpg)

```mdx
<LinkPreview
  url="https://astro.build"
  title="Astro Homepage"
  description="Astro builds fast content sites, powerful web applications, dynamic server APIs, and everything in-between."
  image="https://astro.build/og/astro.jpg"
  theme="x"
/>
```
![x](doc/x.jpg)

```mdx
<LinkPreview
  url="https://astro.build"
  title="Astro Homepage"
  description="Astro builds fast content sites, powerful web applications, dynamic server APIs, and everything in-between."
  image="https://astro.build/og/astro.jpg"
  theme="linkedin"
/>
```
![linkedin](doc/linkedin.jpg)

```mdx
<LinkPreview
  url="https://astro.build"
  title="Astro Homepage"
  description="Astro builds fast content sites, powerful web applications, dynamic server APIs, and everything in-between."
  image="https://astro.build/og/astro.jpg"
  theme="discord"
/>
```
![discord](doc/discord.jpg)

## API


Prop | Type | Default | Description
|---|---|---|---|
url | string (required) | – | Absolute URL to link to.
title | string (required) | "" | – | Heading text (can contain markup).
description | string | "" | Optional descriptive text (truncated to 3 lines except on small).
image | string | null | image / screenshot URL. When omitted, an SVG placeholder is shown.
imageAlt | string | "" | Alt text for the image.
theme | string | "default" | Card style. (`default`, `small`, `facebook`, `x`, `linkedin`, `discord`)

## License
MIT
