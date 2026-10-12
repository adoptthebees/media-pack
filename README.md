# Adopt The Bees — media pack

This repository is the distribution host for the Adopt The Bees media pack: the
brand marks, the site photographs, and the Bee anatomy plate art. The web
application keeps its own build copies under `frontend/src/assets/` in
[`adoptthebees/web`](https://github.com/adoptthebees/web). This repository holds
the same files for partners, press, and any consumer that fetches media over
HTTPS.

## Layout

| Path | Contents | Files |
|------|----------|-------|
| `brand/` | Three bee mark SVGs and the Google "G" for the sign-in button | 4 |
| `photos/` | Nine photographs as responsive WebP renditions (640, 1024, 1600, and where it exists 2400 px) | 29 |
| `plate/` | Bee anatomy plates and studies as WebP renditions (480, 704, 768, 1024, 1200, 1408 px) | 29 |
| `MANIFEST.txt` | Byte count and SHA-256 of every file, tab separated | 62 entries |

## Fetch a file

Raw files are served from GitHub:

```
https://raw.githubusercontent.com/adoptthebees/media-pack/main/<path>
```

Example:

```
https://raw.githubusercontent.com/adoptthebees/media-pack/main/brand/bee-mark-primary.svg
```

To verify a download against `MANIFEST.txt`, compare the SHA-256 of the file
with the value on its line.

## Brand marks

| File | Color | Use |
|------|-------|-----|
| `brand/bee-mark-primary.svg` | Ink | Default mark on light surfaces |
| `brand/bee-mark-inverse.svg` | Honey | Mark on a photo or on an ink surface |
| `brand/bee-mark-mono.svg` | Solid ink | One-color print and single-color use |
| `brand/google-g.webp` | — | Google "G" on the sign-in button only. The mark belongs to Google LLC. |

The three bee marks are flat SVG shapes on a 1056 x 871 grid. Keep the geometry
equal to `beeMark.ts` in the web application. The wordmark is live text. Do not
turn it into an image.

## Photo credits

Every photograph is public domain or CC0. Keep the credit with the file.

| Pack key | Title | Author | License | Source | Retrieved |
|----------|-------|--------|---------|--------|-----------|
| hero | People's Garden Apiary and Pollinator Garden (20130522-NRCS-LSC-0141) | USDA Natural Resources Conservation Service | Public domain | [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:People%27s_Garden_Apiary_and_Pollinator_Garden_(20130522-NRCS-LSC-0141).jpg) | 2026-10-10 |
| goldenFlowers | Steens Mountain - Wildflowers at Kiger Gorge Overlook, 2016 (28665068812) | Bureau of Land Management Oregon and Washington | Public domain | [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Steens_Mountain_-_Wildflowers_at_Kiger_Gorge_Overlook%2C_2016_%2828665068812%29.jpg) | 2026-10-10 |
| honeyBee | Apis mellifera on a fennel flower | Joselodos | CC0 1.0 | [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Apis_mellifera_on_a_fennel_flower.jpg) | 2026-10-10 |
| nativeBee | Blue orchard bee pollinates Zinnia | Scott Bauer, USDA ARS | Public domain | [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Blue_orchard_bee_pollinates_Zinnia.jpg) | 2026-10-10 |
| habitat | Woolly verbena is a wildflower that can be found throughout Kansas Cattle won't eat it because of its bitter taste! (19748407942) | U.S. Fish and Wildlife Service - Midwest Region | Public domain | [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Woolly_verbena_is_a_wildflower_that_can_be_found_throughout_Kansas_Cattle_won%27t_eat_it_because_of_its_bitter_taste%21_%2819748407942%29.jpg) | 2026-10-10 |
| beekeeper | Beekeeper Inspecting the Hive - 51084099207 | Bruce Dupree, Alabama Cooperative Extension System | CC0 1.0 | [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Beekeeper_Inspecting_the_Hive_-_51084099207.jpg) | 2026-10-10 |
| honeycomb | Pollinator Festival at USDA Farmer's Market and Night Farmers Market) (20150619-OSEC-LSC-0227) | U.S. Department of Agriculture | Public domain | [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Pollinator_Festival_at_USDA_Farmer%27s_Market_and_Night_Farmers_Market)_%2820150619-OSEC-LSC-0227%29.jpg) | 2026-10-10 |
| beesOnComb | Queen Bee (16545241268) | U.S. Geological Survey | Public domain | [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Queen_Bee_%2816545241268%29.jpg) | 2026-10-10 |
| urbanGarden | Blanket flower in an urban pollinator garden in Chippewa County, Michigan | Madeleine Cantu, USDA | Public domain | [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Blanket_flower_in_an_urban_pollinator_garden_in_Chippewa_County,_Michigan.jpg) | 2026-10-10 |

A photo rendition is named `<key>-<width>.webp`. The number is the pixel width
of the rendition.

## Plate art

Every plate file is retouched public-domain art. The sources are in
[ATB_AP_001](https://github.com/adoptthebees/web/blob/main/docs/appendix/ATB_AP_001_SOURCES_OWNERSHIP.md):

| Files | Source | Status |
|-------|--------|--------|
| `plate/bee-plate-*.webp` | Stelluti, *Persio tradotto in verso sciolto e dichiarato*, Rome, 1630, page 52, "Descrizzione dell'Ape". Hero engraving | Public domain |
| `plate/queen-plate-*.webp` | Réaumur, *Mémoires pour servir à l'histoire des insectes*, volume 5, Paris, 1740, plate 22, figure 4. Engraved by Cl. Lucas. Wellcome Library scan | Public domain (Wellcome Public Domain Mark) |
| `plate/study-*.webp` | Snodgrass, *The anatomy of the honey bee*, USDA Bureau of Entomology Technical Series 18, 1910, and the Stelluti 1630 volume. ATB_AP_001 gives studies A, D, E, F, and G to Snodgrass and studies B and C to Stelluti | Public domain |

Cowan, *The honey bee*, 1890, gave text facts to the Queen plate only. This
repository holds no art from it.

Retouching removed printed figure numbers, letters, and leader lines from the
source scans.

## Update the pack

1. Change the asset in `adoptthebees/web` under `frontend/src/assets/`.
2. Copy the new file into this repository. Keep the path and the name.
3. Regenerate `MANIFEST.txt`.
4. Commit and push. Raw URLs keep the same path, so consumers do not change.
