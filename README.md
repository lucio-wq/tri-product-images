# TRI Product Images

Image staging repository for TRI Barcelona's product catalogue. Used as source for Shopify CSV imports.

## Structure

```
/hay/
  /3-colour-rug/
  /loop-bin/
  /brew-cup/
  ... (337 product folders total)
```

Each subfolder under `/hay/` corresponds to a unique HAY product, named with the Shopify handle (lowercase, hyphens).

## Naming convention for image files

Inside each product folder, files should follow this pattern:

| Type | Pattern | Example |
|---|---|---|
| Hero / Family (always visible) | `{handle}_family-NN.jpg` | `3-colour-rug_family-01.jpg` |
| Lifestyle per colour | `{handle}_{colour}_lifestyle.jpg` | `3-colour-rug_light-grey_lifestyle.jpg` |
| Detail per colour | `{handle}_{colour}_detail.jpg` | `3-colour-rug_soft-yellow_detail.jpg` |
| Packshot | (from XLS, not stored here) | — |

**Rules:**
- All lowercase
- Words separated by hyphens (`-`), groups by underscores (`_`)
- No spaces, no special characters
- `.jpg` (not `.jpeg`, not `.JPG`)
- Colour names match HAY's PRODUCT NAME 2 field, lowercased and hyphenated

## Image specs

- Max 2500 px on long side (Shopify recommended)
- JPEG quality 88, progressive, no EXIF metadata
- Under 25 MP per file (Shopify hard limit)

## How images are used

1. Drop images into the corresponding `/hay/{handle}/` folder via GitHub Desktop or web
2. Shopify CSV is generated with `raw.githubusercontent.com/lucio-wq/tri-product-images/main/hay/{handle}/{filename}` URLs
3. When CSV is imported to Shopify, Shopify fetches each URL once and copies the image to its own CDN
4. After import, this repo is no longer needed for the live store — it's an archive

## Scope

- 243 HAY Accessories (from Complete List Accessories XLS)
- 94 HAY Lighting (from Complete List Lighting XLS)
- HAY Furniture: pending (XLS not yet processed)
- Other vendors (Santa & Cole, Alessi, Teixidors, etc.): pending

