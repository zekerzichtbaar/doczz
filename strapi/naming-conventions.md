---
sidebar_position: 2
---

# Naming conventions

Standardisatie voor het benamen van components, blocks en velden. Zodat bij het aanroepen van de API het duidelijk is welke casing je moet gebruiken.

## Blocks

Blokken gebruiken **camelCasing**, maar beginnen ook met een hoofdletter. Netzoals React componenten:

```TextImage``` ```Cover``` ```Gallery``` ```Separator``` ```Text``` ```Form``` ```Header``` ```FAQ``` ```Quote```

**LET OP!** De naam die je block geeft in Strapi zal ook de bestandsnaam worden van je component in Next.js

## Componenten

De namen van componenten die je bijvoorbeeld in een block gebruikt maken ook gebruik van **camelCasing** en beginnen ook met een hoofdletter. Deze componenten hebben echter geen relatie met Next.js

```Layout``` ```Content``` ```Button```

## Velden

De namen van velden binnen blocken, componenten en waar dan ook binnen strapi maken gebruik van **snake_casing** dus alles kleine letters met laagstreepjes als spaties.

```layout``` ```content``` ```buttons``` ```title``` ```images``` ```featured_image```  ```background_color```
