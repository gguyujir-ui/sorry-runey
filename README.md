# Apology Website — "i'm sorry, runey..."

A single-page website (everything lives in `index.html`), casual tone for a friend (not romantic):

1. **Landing** — title "Sorry, Bestie..." + Start button
2. **Envelope** — tap to open, then choose **Read** or **I need more time**
3. **Letter** — song automatically tries to play as soon as this screen opens + the letter itself
4. **Forgiveness** — "Will you forgive me?" with Yes / I need more time options
5. **Interactive "Let's Reconnect" game** — tap the high-fives 🤝 that float up to complete the bridge between two friends
6. **Closing** — the promise + a casual, friendly sign-off

## Autoplay music
As soon as the **letter** screen opens, the site automatically tries to play the song set in CONFIG.
If the browser blocks autoplay (some browsers do), the ▶ button on the song card can still be tapped manually.

## How to customize
Everything — text, letter content, and game settings — lives in one place: open `index.html`,
find the **CONFIG** block inside the `<script>` tag, and edit it:

- `letterParagraphs` — the letter content (array of paragraphs)
- `senderName` — the name shown on the letter's signature
- `song` — music filename, title, and artist
- `bridgeTapsNeeded` — how many high-fives are needed to finish the game

Screen titles and other text can be edited directly in each
`<section class="screen" data-screen="...">` block in the HTML.

## Adding music
1. Get an `.mp3` file you have the rights to use.
2. Put it in the same folder as `index.html`, e.g. `song.mp3`.
3. In CONFIG, update:
   ```js
   song: {
     file: "song.mp3",
     title: "Song Title",
     artist: "Artist Name"
   }
   ```

## Deploying to GitHub Pages
1. Create a new GitHub repo, e.g. `sorry-bestie`.
2. Upload `index.html` (and your music file, if any) via "Add file → Upload files".
3. Go to **Settings → Pages**, pick the `main` branch and `/ (root)` folder, then Save.
4. Your site goes live at `https://username.github.io/sorry-bestie/` within a minute or two.
