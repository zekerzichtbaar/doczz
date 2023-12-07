---
sidebar_position: 1
---

# Example Block

Een simpel voorbeeld van een block.

```html title="/components/Blocks/ExampleBlock.vue"

  <template>
    <section class="relative" :class="{'pt-0': block.section.padding_top == false, 'pb-0': block.section.padding_bottom == false}">
        <div class="container">
            <h2>{{ block.title }}</h2>
            <div v-html="block.content"></div>
            
            {buttons.length && (
              <div class="flex flex-wrap gap-4">
                {buttons.map((button, index) => {
                  if(button) {
                    return (
                      // components/Button
                      <Button :key={index} class="some-class" :link="button.link" :type="button.type" :target="button.target">
                        {{button.text}}
                      </Button>
                    )
                  }
                })}
              </div>
            )}
        </div>
    </section>
  </template>
  
  <script setup>
    const { block } = defineProps({
      block: Object,
    })
  </script>
```

Snippet created by [@douwepausma](https://github.com/douwepausma)