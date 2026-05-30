# TRI Product Images

Image repository for TRI Barcelona's product catalogue. Used as staging area for Shopify imports.

## Structure

Each product has its own folder named with the Shopify handle (lowercase, hyphens):

```
/3-colour-rug/
/loop-bin/
/brew-cup/
```

Inside each folder, images follow a strict naming convention — see `NAMING.md` in each product folder.

## How images are used

1. Images are uploaded here by drag & drop from GitHub web UI
2. Raw URLs follow the pattern: `https://raw.githubusercontent.com/lucio-wq/tri-product-images/main/{product-handle}/{filename}`
3. When the Shopify CSV is imported, Shopify fetches each URL once and copies the image to its own CDN
4. After import, this repo is no longer needed for the live store — it's a staging archive

## Public repo

This repo is public so Shopify can fetch images during import. Images are HAY's official press/marketing materials, used by an authorised HAY dealer (TRI Barcelona).
