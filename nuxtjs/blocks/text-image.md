---
sidebar_position: 2
---

# TextImage

```html title="/components/Blocks/TextImage.vue"

<template>
  <section class="relative" :class="{'pt-0': block.section.padding_top == false, 'pb-0': block.section.padding_bottom == false}">
    <div class="container relative z-10">
      <div class="grid lg:grid-cols-12 gap-16 md:gap-24">
        
        <div class="lg:col-span-7" :class="{'order-1 lg:order-1 ': block.alignment === 'TextImage', 'order-1 lg:order-2': block.alignment == 'ImageText'}">
          <div class="relative">
            <div class="aspect-video lg:aspect-[12/14] relative">
              // components/Media
              <Media v-if="block.image.data" :url="block.image.data.attributes.url" :extension="block.image.data.attributes.ext" />
            </div>
          </div>
        </div>
        
        <div class="lg:col-span-5" :class="{'order-2 lg:order-2 ': block.alignment === 'TextImage', 'order-2 lg:order-1': block.alignment == 'ImageText'}">
          <div class="sticky top-24 lg:top-40">
            <h2  v-if="block.title" class="text-xl md:text-2xl lg:text-3xl xl:text-4xl font-black mb-4 md:mb-8">
              {{ block.title }}
            </h2>
            <div v-if="block.content" class="prose prose-invert prose-lg lg:prose-xl">
              <div v-html="block.content"></div>
            </div>
            <div v-if="block.buttons" class="flex flex-col space-y-4 md:space-y-6 items-start mt-4 md:mt-8 lg:mt-12" :class="{'justify-center': block.Type === 'center'}">
              <Button v-for="(button, index) in block.buttons" :key="index" color="light" :to="button.link">
                {{button.text}}
              </Button>
            </div>
          </div>
        </div>
        
      </div>
    </div>
  </section>
</template>

<script setup>
  const { block } = defineProps({
    block: Object,
  })
</script>
```

<!-- Snippet created by [@douwepausma](https://github.com/douwepausma) -->