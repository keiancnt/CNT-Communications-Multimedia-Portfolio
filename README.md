# CNT Multimedia Portfolio

A single-page portfolio for CNT Communications & Multimedia. It opens with the CNT logo intro video on white, which glides into the page logo, then shows every work in a filterable gallery with a full-screen viewer.

Everything is in `index.html`: styles, scripts and the logo images. Nothing needs building or installing.

## Folder layout

```
index.html     the whole site
intro.mp4      the logo video that greets visitors
works/         put your videos and images here
README.md      this file
```

## Publish on GitHub Pages

1. Put these files in the root of a repository and push.
2. On GitHub, open **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, pick `main` and `/ (root)`, then **Save**.
4. After a minute the site is live at `https://<your-username>.github.io/<repo-name>/`.

## Add or edit works

The portfolio is grouped into categories, one for each folder in `portfolio contents`. Open `index.html` and find:

- `CATEGORIES`: the list of categories, in the order they appear on the page. Each is `["id", "Name on the page"]`.
- `YOUR WORKS`: one line per piece, in the order it appears within its category:

```js
{ cat:"social", title:"Singapore", client:"Frontier Travel & Tours", ratio:"2400/2400",
  src:"works/social/singapore.webp", thumb:"works/social/thumb/singapore.webp" },
```

| Field | What it does |
| --- | --- |
| `cat` | The category id it belongs to, from `CATEGORIES`. |
| `title` | Name of the piece. Optional: photos can go without. |
| `client` | Who it was for. Optional. |
| `sub` | A sub-group, for example `"Clothing brand"`. Optional. |
| `src` | The full-size file in `works/` (image, or `.mp4` video). |
| `thumb` | A smaller copy for the grid (about 960px wide). Optional, but it keeps the page fast. |
| `poster` | A still image for a video. |
| `ratio` | Width/height of the piece, for example `"1600/900"`. |
| `duration` | Length of a video, for example `"1:30"`. |
| `featured` | Put `featured:true` on one video to show it as the showreel above the portfolio. |

Each category shows its first 6 pieces, with a "Show all" button for the rest. The counts in the filters, the hero and the About list update automatically.

Save images for the web before adding them: WebP or JPG, about 2400px on the long side (thumbnails about 960px). Videos should be H.264 MP4 at 1080p.

## Tips

- GitHub blocks files over 100 MB and warns over 50 MB. Compress videos for the web (H.264 MP4, 1080p, around 5–10 MB per minute), or host long videos on YouTube or Vimeo and use `embed`.
- To change the greeting, replace `intro.mp4` with a new video of the same size (1920×1080, white background). If the logo sits in a different place at the end, the glide into the page will need adjusting.
- Change the contact address by searching for `corporatehrcomms@cntpromoads.com`.
- Brand colors are set at the top of the `<style>` block: red `#C81020`, hover `#B8141B`, ink `#111111`. The site is white throughout; only the full-screen viewer is dark.
