# omarchy-sbc-theme

<p>
  <a href="https://github.com/tcballard/omarchy-badges"><img alt="Built for Omarchy: Theme" height="20" src="https://raw.githubusercontent.com/tcballard/omarchy-badges/75975e5b5bf75e7ede3764bcd2950046f7abfe2c/badges/v1/omarchy-theme.svg"></a>
  <img alt="Target: Omarchy Quattro" height="20" src="https://img.shields.io/badge/target-Omarchy_Quattro-2f305e?style=flat-square">
  <img alt="Status: development preview" height="20" src="https://img.shields.io/badge/status-development_preview-8a6500?style=flat-square">
</p>

Status: development preview
Intended Omarchy target: Quattro (source revision f4357a3; confirm for this theme)
Tested installed Omarchy version: none

The category badge is a community label, not certification. The target is not a tested-version claim.

**SBC** is a dark theme drawn from the Sunday Builders Club banner by
[@ncfrontiersman](https://x.com/ncfrontiersman): an indigo night sky, a
peach-orange sunrise with violet and coral rays, periwinkle mountains and the
sky-blue "club" lettering.

## Palette

| Role | Colour | From the banner |
| --- | --- | --- |
| background | `#131426` | night sky |
| foreground | `#d6d4fa` | lavender lettering |
| accent / orange | `#fc9464` | the sun |
| magenta | `#b884e0` | violet rays |
| red | `#f4707f` | coral rays |
| blue | `#7f8af2` | lit mountain faces |
| cyan | `#6cc4fc` | "CLUB" lettering |
| selection | `#2f305e` | mountain shadows |

Active windows get a sunrise border that runs from orange to violet
(`hyprland_active_border`); inactive ones fall back to a dim indigo.
Green and yellow are added for terminal use, since the banner has none.

## Wallpapers

Four 3840×2160 WebP backgrounds in two styles, each with and without the club
lettering (see [credits](CREDITS.md) for how they were made). Omarchy shows
them in file-name order, so the first one listed is the default:

- `backgrounds/sunday-omarchy-con-scritta-4k.webp`: Omarchy-style sunset over the lake with the Sunday Builders Club lettering, 3840×2160
- `backgrounds/sunday-omarchy-senza-scritta-4k.webp`: Omarchy-style sunset over the lake without lettering, 3840×2160
- `backgrounds/sunday-retro-con-scritta-4k.webp`: Retro sunburst over the lake with the Sunday Builders Club lettering, 3840×2160
- `backgrounds/sunday-retro-senza-scritta-4k.webp`: Retro sunburst over the lake without lettering, 3840×2160

The Omarchy-style pair is an artistic interpretation of Omarchy Quattro's
landscape backgrounds, not an official Omarchy asset. The retro pair keeps the
banner's sunburst. Both show snow-capped periwinkle mountains, a reflecting
lake and pine forests under a sunset sky.

## Install

For local development, copy this directory to an unused
`~/.config/omarchy/themes/sbc` and select it from the theme menu.
Before applying, record the current theme and background and back up any existing
destination. Do not overwrite a modified installed copy.

Once the repository is published, install it with
`omarchy theme install <repository URL>`. That command applies the theme
immediately and can replace an existing `~/.config/omarchy/themes/sbc`.

## Rollback

Select the previously recorded theme in the theme menu, restore its recorded
background, and restore any backed-up destination. Remove the development copy
only after switching away from it. These instructions still need live verification.

## Media and credits

The four wallpapers were generated with an AI image generator from the Sunday
Builders Club banner, original artwork by
[@ncfrontiersman](https://x.com/ncfrontiersman), resampled to 3840×2160 and
encoded as WebP (quality 95); they are not native 4K renders. Permission to
redistribute them is pending; see [credits](CREDITS.md).
No desktop screenshot is bundled yet, so there is no `preview` image.

Licence: [MIT](LICENSE), for the theme's palette and configuration files. It
does not cover the wallpaper artwork, which is derived from @ncfrontiersman's
banner.

## Application colours

Folder icons use `Yaru-wartybrown`, the same variant Omarchy's built-in Retro 82
theme uses for its peach-orange accent. The Chromium-family browser seed is
`30,29,58`, an intentional indigo tint that matches the background; browser seeds
do not guarantee exact surface colours. Verify Files and an installed browser on
the target desktop.

## Validation limits

See [validation evidence](evidence/checks.tsv). Contrast, image-decoding and
upstream template-rendering checks were run in a build container, not on a
desktop. The Build Omarchy Themes helper rejects the gradient border key by
design (it accepts `#RRGGBB` only); the same palette passes it without that key,
and Omarchy's own renderer handles the gradient. No live desktop, Git-install
or registry acceptance is claimed. The handoff checker checks file/evidence
consistency, not whether recorded commands were actually executed or the theme
looks correct.
