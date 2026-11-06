# Glasswave

Open-source (MIT) liquid-glass music PWA built for low-end phones. No build step: host these files on any HTTPS static host (GitHub Pages works) and open it on your phone.

## Sources
- **Audius** (open catalogue): full-length audio, background playback, Karaoke vocal reduction, visualizer.
- **YouTube** (official APIs only): Google sign-in, search, playlist import, playback in YouTube's own player. YouTube's API policy requires the player to stay visible, so there is no audio-only or background mode for YouTube tracks.

## Setup for YouTube sign-in
1. Google Cloud Console: create a project, enable YouTube Data API v3, create an OAuth Web client ID.
2. Add your site origin as an authorized JavaScript origin.
3. Paste the client ID in Settings.

## Adding a source
Each source needs a search function returning `{src,id,title,artist,art,dur}` and a way to play it (see `play()`). Only add sources whose terms allow third-party playback.

## Known limits
Karaoke is centre-channel vocal reduction (no stems), so results vary by song. Word timing is estimated unless lyrics carry word tags. Social features are link sharing for now; friends and feeds need a backend.
