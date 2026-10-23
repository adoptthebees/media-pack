# Adopt The Bees — media pack

This repository is the official media pack of Adopt The Bees: the bee mark, the
site photographs, the Bee anatomy plate art, and the Home hero film. Press,
partners, and the Adopt The Bees site use these files. The web application keeps
its build copies under `frontend/src/assets/` in
[`adoptthebees/web`](https://github.com/adoptthebees/web). Each copy equals the
file of the release that the site pins.

## Download

Each [release](https://github.com/adoptthebees/media-pack/releases) holds the
whole pack as one ZIP file, `adoptthebees-media-pack-<version>.zip`. The newest
release is at <https://github.com/adoptthebees/media-pack/releases/latest>. The
release notes give the SHA-256 hash of the ZIP.

The ZIP holds every file of this repository at the tag of the release. Each path
in the ZIP starts with `adoptthebees-media-pack-<version>/`.

## Terms of use

[`LICENSE.md`](LICENSE.md) gives the terms of each folder. No single license
covers the whole pack.

## Layout

| Path | Contents | Files |
|------|----------|-------|
| `brand/` | Three bee mark SVGs and the Google "G" for the sign-in button | 4 |
| `photos/` | Ten photographs as responsive WebP renditions (640, 1024, 1600, and where it exists 2400 px) | 32 |
| `plate/` | Bee anatomy plates and studies as WebP renditions (480, 704, 768, 1024, 1200, 1408 px) | 29 |
| `video/` | The Home hero film: a landscape cut (1920 x 1080) and a portrait cut (720 x 1280), each in AV1 and in H.264 | 4 |
| `MANIFEST.txt` | Byte count and SHA-256 of every media file, tab separated | 69 entries |
| `LICENSE.md` | The terms of each folder | — |

## Fetch a file

GitHub serves each file of a release at this address:

```
https://raw.githubusercontent.com/adoptthebees/media-pack/<version>/<path>
```

Example:

```
https://raw.githubusercontent.com/adoptthebees/media-pack/v1.0.0/brand/bee-mark-primary.svg
```

Use `main` in place of the version for the newest commit. A version tag does not
move, so a link with a version keeps its file.

To check a download, compare the SHA-256 hash of the file with the value on its
line in `MANIFEST.txt`.

## Versions

A version has the form `vMAJOR.MINOR.PATCH`.

| Change | Part that goes up |
|--------|-------------------|
| A release removes or renames a path | MAJOR |
| A release adds a file or changes the content of a file | MINOR |
| A release changes only `README.md` or `LICENSE.md` | PATCH |

A published release does not change. A correction is a new version.

## Brand marks

| File | Color | Use |
|------|-------|-----|
| `brand/bee-mark-primary.svg` | Ink | Default mark on light surfaces |
| `brand/bee-mark-inverse.svg` | Honey | Mark on a photo or on an ink surface |
| `brand/bee-mark-mono.svg` | Solid ink | One-color print and single-color use |
| `brand/google-g.webp` | — | Google "G" on the sign-in button only. Google LLC owns the mark. This pack gives no right to use it. |

The three bee marks are flat SVG shapes on a 1056 x 871 grid. Keep the geometry
equal to `beeMark.ts` in the web application. The wordmark is live text. Do not
turn it into an image.

## Photo credits

Every photograph is public domain or CC0. Keep the credit with the file.

| Pack key | Title | Author | License | Source | Retrieved |
|----------|-------|--------|---------|--------|-----------|
| hero | Honey bee on red zinnia flower (D4114-1) | Peggy Greb, USDA/ARS | Public domain | [USDA ARS](https://www.ars.usda.gov/oc/images/photos/featuredphoto/jun21/honeybee) | 2026-10-12 |
| goldenFlowers | Steens Mountain - Wildflowers at Kiger Gorge Overlook, 2016 (28665068812) | Bureau of Land Management Oregon and Washington | Public domain | [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Steens_Mountain_-_Wildflowers_at_Kiger_Gorge_Overlook%2C_2016_%2828665068812%29.jpg) | 2026-10-10 |
| honeyBee | Apis mellifera on a fennel flower | Joselodos | CC0 1.0 | [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Apis_mellifera_on_a_fennel_flower.jpg) | 2026-10-10 |
| nativeBee | Blue orchard bee pollinates Zinnia | Scott Bauer, USDA ARS | Public domain | [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Blue_orchard_bee_pollinates_Zinnia.jpg) | 2026-10-10 |
| habitat | Woolly verbena is a wildflower that can be found throughout Kansas Cattle won't eat it because of its bitter taste! (19748407942) | U.S. Fish and Wildlife Service - Midwest Region | Public domain | [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Woolly_verbena_is_a_wildflower_that_can_be_found_throughout_Kansas_Cattle_won%27t_eat_it_because_of_its_bitter_taste%21_%2819748407942%29.jpg) | 2026-10-10 |
| beekeeper | Beekeeper Inspecting the Hive - 51084099207 | Bruce Dupree, Alabama Cooperative Extension System | CC0 1.0 | [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Beekeeper_Inspecting_the_Hive_-_51084099207.jpg) | 2026-10-10 |
| honeycomb | Pollinator Festival at USDA Farmer's Market and Night Farmers Market) (20150619-OSEC-LSC-0227) | U.S. Department of Agriculture | Public domain | [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Pollinator_Festival_at_USDA_Farmer%27s_Market_and_Night_Farmers_Market)_%2820150619-OSEC-LSC-0227%29.jpg) | 2026-10-10 |
| beesOnComb | Queen Bee (16545241268) | U.S. Geological Survey | Public domain | [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Queen_Bee_%2816545241268%29.jpg) | 2026-10-10 |
| urbanGarden | Blanket flower in an urban pollinator garden in Chippewa County, Michigan | Madeleine Cantu, USDA | Public domain | [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Blanket_flower_in_an_urban_pollinator_garden_in_Chippewa_County,_Michigan.jpg) | 2026-10-10 |
| volunteers | Volunteer Group Planting at Logan Pass 08 (28187658192) | Jacob W. Frank, National Park Service | Public domain | [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Volunteer_Group_Planting_at_Logan_Pass_08_%2828187658192%29.jpg) | 2026-10-23 |

A photo rendition is named `<name>-<width>.webp`. The name is the pack key in
lowercase words with hyphens, for example `bees-on-comb` for `beesOnComb`. The
number is the pixel width of the rendition.

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

## Hero film

The Home hero film is an edit of eight short clips from Pexels and Pixabay. The
clips are not public domain or CC0. The product owner approved the Pexels
License and the Pixabay Content License for this film only (ATB_TD_012 section
5 in the web repository). The licenses do not allow a clip to be published on
its own, so this repository holds only the edited film, never a source clip.

`frontend/src/assets/video/heroFilm.json` in the web repository holds the edit
list and the credit of each clip. `npm run build:hero-film` in the web
repository rebuilds the four files.

| Clip | Author | License | Source |
|------|--------|---------|--------|
| Flowers, Butterflies, Sunrays | Joe_hackney | Pixabay Content License | [Pixabay](https://pixabay.com/videos/flowers-butterflies-sunrays-forest-124099/) |
| Bee, Insect, Blossom | RoyBuri | Pixabay Content License | [Pixabay](https://pixabay.com/videos/bee-insect-blossom-bloom-honey-bee-56238/) |
| Buzzing Beehive in Garden Close-Up | Robert Schwarz | Pexels License | [Pexels](https://www.pexels.com/video/buzzing-beehive-in-garden-close-up-31913044/) |
| A Beekeeper Inspecting a Hive Frame | ROMAN ODINTSOV | Pexels License | [Pexels](https://www.pexels.com/video/a-beekeeper-inspecting-a-hive-frame-8841379/) |
| Close-Up of Bees on Wooden Honeycomb Frame | Hakan Kayahan | Pexels License | [Pexels](https://www.pexels.com/video/close-up-of-bees-on-wooden-honeycomb-frame-33338624/) |
| Close up of a Beekeeper Holding a Hive Frame | ROMAN ODINTSOV | Pexels License | [Pexels](https://www.pexels.com/video/close-up-of-a-beekeeper-holding-a-hive-frame-8841376/) |
| Close-up of Bees Entering a Beehive at Dusk | Robert Schwarz | Pexels License | [Pexels](https://www.pexels.com/video/close-up-of-bees-entering-a-beehive-at-dusk-31912930/) |
| Bumblebee Pollinating Purple Wildflower | Thierry Rossier | Pexels License | [Pexels](https://www.pexels.com/video/bumblebee-pollinating-purple-wildflower-32723496/) |

## Update the pack

This repository holds no code. The scripts live in `adoptthebees/web`. Run each
command in the root of a checkout of `adoptthebees/web`. Keep this repository
beside it as `media-pack`, or set `ATB_MEDIA_PACK_DIR` to its path.

1. Change the asset in `adoptthebees/web` under `frontend/src/assets/`.
2. Copy the new file into this repository. Keep the path and the name.
3. Run `npm run build:media-manifest`. It writes `MANIFEST.txt` here.
4. Commit and push this repository.
5. Run `npm run release:media-pack -- <version> --dry-run`. When each check
   passes, run it again without `--dry-run`. The command publishes the release
   with its ZIP and pins the site to it in `frontend/src/assets/mediaPack.json`.
6. Run `npm run sync:media`, then commit `adoptthebees/web`.
