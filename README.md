# Lineup Guide

A fast, good-looking site for keeping **your own Valorant lineups** in one place, organised by agent and map. Every lineup is a short set of steps with screenshots, so you can look one up in seconds and learn it properly.

No build step, no server, no account: it's one HTML file and one settings file.

<p align="center">
  <img src="docs/home.png" alt="Lineup Guide home page" width="760">
</p>
<p align="center">
  <img src="docs/lineups.png" alt="Brimstone lineups on Corrode" width="760">
</p>

## Features

- **Browse your way:** header menus for agents and the current map pool, plus arrows to step to the next or previous agent or map.
- **Filters:** mode (Offense/Defense), site (A/B/C) and side (CT/T).
- **Lineup steps:** *Go to this area*, *Aim here* and *To get this*, each with text and an image. Click any image to zoom.
- **Descriptions and pictures** for every agent and map, built in and editable.
- **Search** across agents, maps and lineup titles, including ones you have hidden.
- **Study tools:** favourites, a Random lineup button, Previous/Next (arrow keys work too), notes on each lineup and an image annotator.
- **Switch agents and maps on or off** without touching code, so the site only shows what you play right now.
- **Share lineups** with friends as a single file, and import theirs.
- **Backup, restore and auto-save** to a file on your computer.
- Works on phones.

## Quick start (on your computer)

1. Download or clone this repo.
2. Keep `index.html` and `config.js` **in the same folder**.
3. Open `index.html` in Edge or Chrome.

> If you downloaded a zip, extract it first. Opening the page from inside the zip leaves `config.js` behind.

## Host it on GitHub Pages

1. Create a new repository and upload `index.html`, `config.js` and the `docs` folder.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, pick `main` and `/ (root)`, then save.
4. After a minute your site is live at `https://YOUR-USERNAME.github.io/YOUR-REPO/`.

Visitors see the built-in descriptions and images but start with no lineups. Lineups are stored in each person's own browser (see [Where your data lives](#where-your-data-lives)).

## Choosing agents and maps

There are two ways, and both do the same thing:

| Where | How |
| --- | --- |
| **`config.js`** | Set a name to `true` (shown) or `false` (hidden), save, refresh. This is the starting point. |
| **Settings (gear icon)** | Tick or untick agents and maps and press **Save settings**. These choices are remembered in your browser and win over `config.js`. **Reset to config.js** goes back to the file. |

Hidden agents and maps keep their lineups. Turn them back on and everything returns. Search still finds hidden ones.

## Adding lineups

1. Press **+ Add lineup**.
2. Pick the agent, map, mode, site and side, then give it a title.
3. Fill in the three steps. For each image, click the box to choose a file, drag one in, or paste a screenshot with Ctrl+V.
4. Save.

Images are shrunk automatically so the site stays quick.

**Editing descriptions and pictures:** open an agent or map page and press **Edit info**. **Settings → Reset descriptions** restores the built-in ones.

## Sharing lineups

Open **Settings → Share lineups**.

- **Export:** choose an agent and map (or *All*), optionally add your name as credit, and press **Export lineups**. You get one small file to send to a friend. Your favourites are not included. Tick the box to include agent and map descriptions too.
- **Single lineup:** open it and press **Share**.
- **Import:** press **Import lineups** and pick a file. You're told how many are new, duplicates are skipped, and if the lineups belong to a hidden agent or map you're offered to turn it on.

## Backups and auto-save

In **Settings**:

- **Backup** downloads everything (lineups, descriptions, images) as one file. **Restore** adds it back and skips duplicates.
- **Auto-save to a file** keeps a file on your computer up to date as you work. Choose or create the file once, and putting it in a OneDrive or Dropbox folder gives you a free offsite copy. It needs desktop Edge or Chrome, and after reopening the browser it asks you to reconnect with one click.

## Where your data lives

Lineups are saved **in your browser** (IndexedDB), not in the HTML file and not on GitHub. That means:

- Each browser and each device has its own copy, and a hosted site opens empty the first time.
- Clearing site data wipes it, so keep a backup or turn on auto-save.
- Move lineups between devices with **Export lineups** and **Import lineups**, or **Backup** and **Restore**.

## Using it on your phone

Open the GitHub Pages link in your phone browser. Things to know:

- Auto-save to a file isn't available on phones, and paste and drag-and-drop don't exist on touch (picking from your gallery works).
- iPhone Safari may erase a website's saved data after about a week without visits unless it's added to your Home Screen. Add it to the Home Screen and keep a backup.
- Lineups don't sync between devices. Use the share or backup files.

## Project files

```
index.html   the whole site (code, styles, built-in descriptions and images)
config.js    which agents and maps are switched on
docs/        screenshots used in this README
```

## Disclaimer

Lineup Guide was created under Riot Games' "Legal Jibber Jabber" policy using assets owned by Riot Games. Riot Games does not endorse or sponsor this project. VALORANT and all related names, agent and map artwork and descriptions are the property of Riot Games.
