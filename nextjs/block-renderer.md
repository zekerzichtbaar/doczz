---
sidebar_position: 2
---

# Block Renderer

Rendererd blocks uit een Dynamic Zone in Strapi.

```js
// /app/BlockRenderer.js

import Blocks from "./blocks";

function formatBlockName(string) {
  let output = string.replace('blocks.', '');

  // Convert kebab case to camel case
  output = output.replace(/-([a-z])/g, function (match, letter) {
    return letter.toUpperCase();
  });

  // Capitalize the first letter
  output = output.replace(/^\w/, function (match) {
    return match.toUpperCase();
  });

  return output;
}
  
export default function BlockRenderer({searchParams, blocks}) {
  let output = blocks.map((block) => {
    const BlockName = formatBlockName(block.__component);
    const BlockTag = Blocks[BlockName];
    if(BlockTag != undefined) {
      return (<BlockTag searchParams={searchParams} blockData={block} />)
    }
  })
    
  return output;
}
```

```js
// /app/blocks/index.js

import Separator from "/app/blocks/Separator";
import TextImage from "/app/blocks/TextImage";
import Video from "/app/blocks/Video";
import Gallery from "/app/blocks/Gallery";

export default {
  Separator,
  TextImage,
  Video,
  Gallery
};
```

Snippets created by [@douwepausma](https://github.com/douwepausma)