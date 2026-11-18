# Cat Moon Portfolio

**Live demo: https://thisisconnielin.github.io/**

A Claude skill and template for a personal site where a sticker cat walks on a photoreal moon you can drag. Projects stand on the horizon and open as cards. Films play inside them. Small "things I love" stickers bounce, drive and float, each with a tap-to-read fun fact, and a paper plane tows your socials across the sky. Soft generated moon music plays in the background. It is a static site with no build step and no dependencies: one HTML file and a canvas. GitHub Pages serves it as-is.

## Install

In Claude Code:

```
/plugin marketplace add thisisconnielin/cat-moon-portfolio
/plugin install cat-moon-portfolio@cat-moon-portfolio
```

Then ask *"make me a cat moon portfolio"*. Claude copies this template and asks for your name, projects, socials and favorite things. It swaps them in and deploys the site to `https://<you>.github.io/`.

**By hand:** click **Use this template** on GitHub, name the new repo `<you>.github.io`, then follow [`skills/cat-moon-portfolio/SKILL.md`](skills/cat-moon-portfolio/SKILL.md).

## Local preview

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Structure

- `index.html` — the whole site: layout, motion, sound, and all content (projects, cards, stickers, socials)
- `assets/` — moon texture, galaxy, the cat, project and toy stickers (transparent PNG / WebP)
- `media/` — films, posters and screenshots shown in the cards (replace with your own)
- `tools/` — scripts that made the art: cut stickers out of one render (`cut_ref.py`), wrap a moon texture (`make_moon.py`), slice generated sticker sheets (`slice.py`), and the image prompt (`codex-assets-prompt.md`)
- `skills/cat-moon-portfolio/` — the Claude skill

## Notes

- Drag, swipe, scroll or use ← → to turn the moon. Tap a project to open it, tap a sticker for a fun fact.
- Music starts after the first tap (browser rule) and can be turned off with ♪.
- Stickers still showing as emoji are placeholders until their art is generated.

Made by [Connie Lin](https://github.com/thisisconnielin), with Claude as co-writer.
