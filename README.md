# Adam's Football Portfolio ⚽

A single-file mini site introducing Adam and his football journey — Canada → Madrid → the future.

## How to view it

Just open `index.html` in any browser (double-click it), or serve it locally:

```bash
python3 -m http.server 8080
# then open http://localhost:8080
```

## How to edit content

Everything editable lives in **one place**: the `PLAYER` object near the bottom of `index.html` (look for "EDIT EVERYTHING HERE").

- **Shirt number & contact email** — top of the `PLAYER` object.
- **Player details** (age, position, foot, club…) — the `stats` list.
- **Journey timeline** — the `timeline` list. Add a new entry whenever there's news.
- **Videos** — the `videos` list. Each entry is one of two kinds:
  - **Embedded from another site**: `{ url: 'https://...', title: {...}, desc: {...} }`
    — just paste the video's normal link. YouTube (including Shorts and
    youtu.be links), Vimeo and Dailymotion are converted automatically.
    For other platforms (Veo, Hudl, …) use the platform's "embed" link as the url.
  - **Uploaded file**: `{ file: 'media/my-clip.mp4', title: {...}, desc: {...} }`
    — drop the video file into the `media/` folder first.
  - (Until you have a video, `{ placeholder: true, title: {...}, desc: {...} }`
    shows a "coming soon" card.)

## Photos & videos

Drop Adam's photo and video files into the `media/` folder:

- **Profile photo**: save it as `media/adam.jpg`, then in `index.html` find the
  `player-photo` div and replace the placeholder `<span>` with
  `<img src="media/adam.jpg" alt="Adam">` (there's a comment showing exactly this).
- **Videos**: put `.mp4` files in `media/` and reference them from the `videos` list.

## Languages

The site is bilingual — the EN/ES toggle is in the top-right corner, and the
choice is remembered between visits. All fixed text lives in the `I18N` object
in `index.html` if you want to tweak wording.

## Publishing

The whole site is static files, so any free static host works:
[Netlify Drop](https://app.netlify.com/drop) (drag the folder in), GitHub Pages,
or Vercel. Keep videos under ~50 MB each for smooth hosting, or use YouTube
(unlisted videos work great for this).
