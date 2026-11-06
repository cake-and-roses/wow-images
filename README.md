# wow-images

The textures that make up the World of Warcraft user interface, for both
game versions:

| Folder | Game | Build | Images |
| --- | --- | --- | --- |
| [`Retail/`](Retail) | World of Warcraft | 12.1.5.70783 | 142,793 |
| [`Forever/`](Forever) | World of Warcraft: Forever | 1.60.1.70790 | 134,186 |

Each folder mirrors the client's `Interface/` directory, keeping Blizzard's
original folder and file names. For example, `Interface/ICONS/INV_Misc_QuestionMark.blp`
is `Retail/ICONS/INV_Misc_QuestionMark.png`.

This follows the layout of [Valithriann/Interface](https://github.com/Valithriann/Interface).

## How the images were made

1. Each client was launched with `-console`, and `exportInterfaceFiles art`
   was run at the login screen. This writes the interface textures to
   `BlizzardInterfaceArt/Interface/` next to the game executable.
2. Every `.blp` file was converted to `.png` with [Pillow](https://python-pillow.org/).
   Pillow can't read uncompressed BGRA BLPs (BLP2 encoding 3), so those were
   decoded directly from their pixel data.

You can view the original `.blp` files with [BLPView](https://www.wowinterface.com/downloads/info16700-BLPView.html)
(Windows) or [BLPLook](https://www.wowinterface.com/downloads/info9011-BLPLook.html) (macOS).

## Legal

All images are the property of Blizzard Entertainment, Inc. World of Warcraft
and Blizzard Entertainment are trademarks or registered trademarks of Blizzard
Entertainment, Inc. This repository is not affiliated with or endorsed by
Blizzard Entertainment.
