# Web Clipper setup (≈10 minutes, one time)

1. Install **Obsidian Web Clipper** from the Chrome Web Store (official, by Obsidian).
2. In Obsidian: **Open folder as vault** → this folder.
3. Clipper → Settings (cog) → Templates → **Import** → `marketing-leadership-os-clip.json`. Drag it to the **top** of the template list so it's the default.
4. In that template, set **Vault** to this vault's name, so clips never land in another vault.
5. **Leave Interpreter off.** No API key is needed: the clip saves the full text, and `/process-inbox` writes the takeaways and tags afterwards on your Claude plan.
6. Test on one Substack post and one blog post. Check that `author` and `published` came through. Where a site's metadata is poor (LinkedIn posts), fix those two by hand in `/process-inbox`.

**Clip a passage, not a page:** highlight with the Clipper's highlighter first and the note keeps your highlights. That's usually worth more than the full text.

## Swipe template (2 minutes)

1. Clipper → Settings → Templates → **Import** → `marketing-leadership-os-swipe.json`. Keep it *below* the clip template, so clips stay the default.
2. Set **Vault** to this vault's name.
3. To save an example: open the page, switch the Clipper to **Marketing Leadership OS — Swipe**, highlight the bit you like, and add a line on why you saved it. For an ad or an image, a screenshot dropped into `inbox/swipe/` works just as well.
4. On mobile: save the screenshot into `inbox/swipe/` (for example through iCloud Drive or Dropbox), or, if you've connected Gmail to Claude, email it to yourself with the subject **swipe** and `/process-swipe` picks it up.
