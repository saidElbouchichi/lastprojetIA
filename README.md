# StudioPro 🎵

A fully functional **Spotify-inspired music player** built as a single HTML file — no dependencies, no build step, no server required.

---

## ✨ Features

| Feature | Details |
|---|---|
| 🎨 Spotify UI | 3-panel layout (sidebar, main, player bar) with Spotify's exact color palette |
| ▶️ Audio Playback | Real MP3 streaming via the HTML5 `<audio>` API |
| 🔀 Shuffle | Randomizes the play queue |
| 🔁 Repeat | Loops the current track (`audio.loop`) |
| 🔇 Mute / Volume | Slider + mute toggle |
| ❤️ Liked Songs | Like/unlike tracks, persisted in `localStorage` |
| 🔎 Search | Real-time filter across title, artist, and album |
| 📚 Library | Dedicated view listing all liked songs |
| 📊 Visualizer | Web Audio API frequency bars (falls back to random animation) |
| 💿 Spinning CD | CSS `@keyframes` disc that rotates while playing |
| ⌨️ Keyboard | `Space` = play/pause · `→` = next · `←` = prev |
| 📱 Responsive | Collapses sidebar to icon-only at ≤ 900 px |

---

## 🎨 Color Palette

```
#1DB954  →  Spotify Green   (accent, buttons, active states, EQ bars)
#121212  →  Deep Black      (app background)
#181818  →  Dark            (sidebar panels, main panel)
#242424  →  Surface         (cards, track rows)
#FFFFFF  →  White           (primary text, play button)
#A7A7A7  →  Muted Grey      (secondary text, inactive icons)
```

Only **3 core tones** — green, black, white — kept strictly homogeneous.

---

## 📁 File Structure

```
studiopro.html          ← entire app (HTML + CSS + JS, single file)
README.md               ← this file
```

### Inside `studiopro.html`

```
Lines   1–6      DOCTYPE, lang="en", meta, title
Lines   7–418    <style> — all CSS (variables, layout, components)
Lines 419–589    HTML body (sidebar, main views, player bar)
Lines 590–595    Toast + <audio> element
Lines 596–1118   <script> — all JavaScript
```

---

## 🚀 Usage

Just open the file in any modern browser:

```bash
open studiopro.html
# or drag-and-drop into Chrome / Firefox / Safari / Edge
```

No npm, no bundler, no internet required (except for the demo cover images from `picsum.photos` and audio streams from `soundhelix.com`).

---

## 🎵 Demo Tracks

8 royalty-free sample tracks from [SoundHelix](https://www.soundhelix.com), with procedurally generated cover art from [Picsum](https://picsum.photos):

| # | Title | Artist | Album |
|---|---|---|---|
| 1 | Neon Skyline | Aurora Sound | Midnight Drive |
| 2 | Electric Dunes | Sahara Pulse | Desert Wave |
| 3 | Cobalt Dreams | Lunar Tide | Blue Hour |
| 4 | Velvet Echoes | Nova Bloom | Soft Static |
| 5 | Solar Mirage | Helios Beats | Sun Cycle |
| 6 | Crystal Currents | Echo Mirage | Prism |
| 7 | Phantom Heart | Vivid Static | Afterglow |
| 8 | Midnight Garden | Ivory Tide | Silver Bloom |

---

## 🛠 Customization

### Add your own tracks

Edit the `tracks` array in the `<script>` section:

```js
const tracks = [
  {
    id: 9,
    title: "My Song",
    artist: "My Artist",
    album: "My Album",
    duration: "3:30",
    cover: "https://example.com/cover.jpg",
    src: "https://example.com/audio.mp3"
  },
  // ...
];
```

### Change the accent color

Edit the CSS variable in `:root`:

```css
:root {
  --green: #1db954;   /* swap for any hex */
}
```

---

## 🧱 Tech Stack

- **HTML5** — semantic structure
- **CSS3** — Grid layout, custom properties, `@keyframes`, `backdrop-filter`
- **Vanilla JS** — no frameworks, no libraries
- **Web Audio API** — real-time frequency visualizer
- **localStorage** — persistent liked songs

---

## 📄 License

Free to use and modify for personal and educational projects.
