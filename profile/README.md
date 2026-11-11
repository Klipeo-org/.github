# Klipeo

Klipeo is a video editor with a crew of AI agents. You describe the video you want, and the crew
edits it on a real multitrack timeline. Scout browses and checks footage, Snip cuts and trims, Zip
adds motion and titles, Echo handles sound and music, Cue writes captions, Tint grades colour,
Spark generates new images and video, and Ship exports. You can edit anything by hand at any time.

## Where to use it

| App | Current version | Get it |
| --- | --- | --- |
| Web app | Latest | [klipeo.com](https://klipeo.com) |
| Mac app (macOS 14 or later) | 0.5.3 | [klipeo.com/download](https://klipeo.com/download) |
| Chrome extension (Chrome 118 or later) | 0.1.2 | [Chrome Web Store](https://chromewebstore.google.com/detail/klipeo-screen-recorder/phohjbafgdnblgbbhdamedjjmknmdjlf) or the [release zip](https://github.com/Klipeo-org/klipeo/releases/tag/extension-v0.1.2) |
| Android app (Android 7.0 or later) | 0.1.5 | [APK on GitHub](https://github.com/Klipeo-org/klipeo/releases/tag/android-v0.1.5) |
| Bridge CLI | 0.1.5 | `npm i -g @bytehumi/klipeo-bridge`, then run `klipeo` |

The Mac app is signed with Developer ID, notarized by Apple, and updates itself. The Chrome
extension records a tab and sends the take to the open Klipeo editor. The Chrome Web Store
listing updates to 0.1.2 after store review; until then, load the release zip unpacked. The
Android app is installed from the APK; it is not on Google Play yet. The bridge CLI connects your
own Claude Code, Codex, Gemini CLI, or OpenCode to Klipeo's Vibe mode.

All builds are on the [Klipeo releases page](https://github.com/Klipeo-org/klipeo/releases).

## How it is built

- Web app and API: Next.js 16 and React 19 on Vercel.
- Database: PostgreSQL with Drizzle ORM on Neon, for both staging and production.
- Media: Cloudflare R2 for large uploads and the media library, with Appwrite for small uploads.
- Background work: Cloudflare Workers for event streaming, scheduling, and library thumbnails,
  and Cloudflare Containers for the hosted agent, scene detection, and short video processing.
  Media workers run on AWS.
- Mac app: SwiftUI. Android app: Expo and React Native. Chrome extension: WXT.

## Links

- Website: [klipeo.com](https://klipeo.com)
- Docs: [klipeo.com/docs](https://klipeo.com/docs)
- Changelog: [klipeo.com/changelog](https://klipeo.com/changelog)
