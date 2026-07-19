# How to Update This Website (No Code Required)

Almost everything on the site lives in ONE file: `content.json`.
You edit that file, the site updates. You never touch HTML.

## The 60-Second Edit

1. Go to: https://github.com/Mryan-eng/frontrangerf.org/edit/main/content.json
   (or open content.json in the repo and click the pencil icon)
2. Find the text you want to change. Everything is `"label": "value"` pairs.
3. Change the text BETWEEN the quotes. Don't delete the quotes or commas.
4. Click the green "Commit changes" button (top right), then confirm.
5. Wait 1-2 minutes. Hard-refresh the site (Ctrl+Shift+R). Done.

This also works from your phone in a browser.

## What's In content.json

- `tagline` — the sentence under the homepage title
- `stats` — the four boxes (callsign, license, founded, location)
- `research` — every research project card. `summary` shows on the
  homepage, `description` is the longer text on the research page.
  `statusClass` must be one of: `active`, `draft`, `done`
- `publications` — the publications table. `statusClass` must be
  `draft` (orange) or `published` (green)
- `projects` — everything on the Personal Projects page

## Adding a New Project or Publication

Copy an existing block from `{` to `}`, paste it after the last one,
add a comma between blocks, and change the text. Example:

    { "existing": "block" },   <- comma added here
    { "your": "new block" }

## Rules That Prevent Breakage

- Keep all quotes `"` and commas exactly as they are
- No comma after the LAST item in a list
- Don't use bare double-quotes inside your text (use ' instead)
- If the site suddenly shows old/fallback content, your JSON has a
  typo — paste content.json into https://jsonlint.com to find it

## What This File Does NOT Control

The Portfolio and Contact pages, and page layout/colors, are still
in the HTML files. They rarely change. To edit them: open the .html
file on GitHub, click the pencil, edit the visible text, commit.

## If You Break Something

Nothing is ever lost. In the repo, click "History" on content.json,
open the last good version, copy it, and paste it over the broken one.
