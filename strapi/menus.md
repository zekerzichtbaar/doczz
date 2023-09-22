---
sidebar_position: 2
---

# Menu's


## Installatie

Voor menus maken we gebruik van de [Menus plugin](https://market.strapi.io/plugins/strapi-plugin-menus).

```yarn add strapi-plugin-menus@latest```

## Slugs

De slugs die je instelt voor menu's maken gebruik van **kebab-casing**

### Voorbeeld

Zorg ervoor dat je de slugs van menu's niet de naam geeft van de titel die er boven staat, maar een algemene naam geeft over de positie. Zo kan later zonder verwarring de titel worden aangepast.

- **Topbar menu** ```topbar```
- **Hoofdmenu** ```primary```
- **Footer** ```footer```
    - **Bij meerdere menus** ```footer-1``` ```footer-2```
- **Sub footer** ```sub-footer```