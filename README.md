# 💌 A letter for Grace

An interactive, single-file love letter website. Open the envelope → read the letter → see the
reasons → scroll through your pictures → end on a love note that's always been true (the "No" button is lying 😄).

Everything lives in one file (`index.html`) — no framework, no build step, no account needed.

## ✏️ How to personalize it

Open `index.html` and edit only the `const CONFIG = { ... }` block near the top of the script.

| What | Where in `CONFIG` |
|---|---|
| Opening screen (big cursive "Grace,") | `introTitle` |
| Letter salutation + paragraphs | `letter.salutation`, `letter.paragraphs` |
| Your signature | `from` (put your real name here) |
| "Why I like you" list | `reasons` (add/remove lines) |
| The closing card wording | `question` |
| Celebration wording | `celebration` |

The letter is already addressed to Grace — rewrite every paragraph in your own voice. Short and
honest reads better than flowery.

### Your photos
All 11 pictures are **embedded directly inside `index.html`** (base64), so the file is fully
self-contained — send just this one file and the photos come with it. The originals also sit in
the `photos/` folder as a backup.

To swap or add a photo, send me the new picture and I'll re-embed it, or edit each entry's
`caption` in `CONFIG.memories` so it matches its photo.

### The song player
On the last card (after she says yes), the page asks **"want to keep listening to the song?"** and
shows a little music player with the album art, artist and track name, play/pause/restart controls,
and a progress bar you can tap to jump anywhere in the song. The song plays all the way through
(no looping), so every second gets heard — and if she replays it, it starts again from the top.

To change any of it, edit `CONFIG`:

| What | Where in `CONFIG` |
|---|---|
| The audio file | `musicFile` (put your `.mp3` next to `index.html`) |
| Artist name | `song.artist` |
| Song title | `song.title` |
| Album art picture | `song.art` (drop a photo in `photos/`, e.g. `photos/album-art.jpg`) |
| The question above the player | `song.ask` |

Details:
1. Put your audio file next to `index.html` (an `.mp3` is easiest) and set `musicFile`.
2. The song starts when Grace taps the envelope (browsers need that tap to allow sound). The
   speaker button in the corner pauses/resumes it, and only appears once the song is actually
   playing — no music means no button, no fake sounds.
3. The corner button and the "keep listening" player control the same song, so she never loses
   her place in the track.

## 🚀 Sharing it

The fastest way to get a link your phone can open:

1. **Netlify Drop** — go to <https://app.netlify.com/drop> and drag the whole folder in. Public link in seconds.
2. **GitHub Pages** — push the folder to a repo, enable Pages, share the URL.
3. **Just send the file** — `index.html` runs on its own (double-click to open). Google Fonts need
   internet and fall back to system fonts offline.

Made with 💖 for Grace.
