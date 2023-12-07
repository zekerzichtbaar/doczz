---
sidebar_position: 1
---

# Example Block

Een simpel voorbeeld van een block.

```jsx
// /app/blocks/ExampleBlock.js

import Button from '@/app/components/Button'

export default function ExampleBlock({ blockData: { layout, content, buttons, some_other_field } }) {
    return (
        <section className={`relative bg-${layout.background_color} ${layout.padding_top == 'none' ? 'pt-0' : ''} ${layout.padding_bottom == 'none' ? 'pb-0' : ''}`}>
            <div className="container">
                {/* Check if field has value before rendering element */}
                {content.subtitle && <span>{content.subtitle}</span>}
                {content.title && <h2>{content.title}</h2>}
                {content.content && <p>{content.content}</p>}

                {/* Rendering an array of buttons */}
                {buttons.length && buttons.map((button, index) => (
                  <Button className="some-class" key={index} link={button.link} type={button.type} target={button.target}>
                    {button?.text}
                  </Button>
                ))}
            </div>
        </section>
    )
}
```

Snippet created by [@douwepausma](https://github.com/douwepausma)