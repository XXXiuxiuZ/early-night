# Early Night – install on iPhone

1. Host this folder on any HTTPS static host (GitHub Pages, Netlify Drop, Vercel). Drag-and-drop the folder on https://app.netlify.com/drop is the fastest.
2. Open the URL in **Safari** on your iPhone.
3. Tap Share › **Add to Home Screen**. Open it from the Home Screen icon.
4. In Settings inside the app: tap **Add nightly reminder to Calendar** (a repeating alert at wind-down time), and optionally set up the Shortcuts automation described there.

Progress is stored on the device (localStorage).

## Why no alarm / push?
iOS doesn't let web apps set Clock alarms or schedule local notifications. Web Push works for Home Screen apps on iOS 16.4+, but needs a server to send at the right time. If you want that later: add a small backend (e.g. a Vercel cron + the `web-push` library) that stores the push subscription and the user's wind-down time.
