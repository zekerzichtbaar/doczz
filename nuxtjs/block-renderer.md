---
sidebar_position: 2
---

# Block Renderer

Rendererd blocks uit een Dynamic Zone in Strapi.

```js
// /components/BlockRenderer.vue

<template>
  <div v-for="block in blocks" :key="block.id">
    <BlocksHeader v-if="block.__typename == 'ComponentBlocksHeader'" :block="block" />
    <BlocksTextImage v-else-if="block.__typename == 'ComponentBlocksTextImage'" :block="block" />
  </div>
</template>

<script setup>
  const { blocks } = defineProps({
    blocks: Object,
  })
</script>
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