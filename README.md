# NewsWave — News website starter

A responsive, static news website designed to publish on **GitHub Pages**. It includes:
- Homepage with a featured story and latest-news grid
- Categories and live search
- Article detail pop-up with publish date, author, reading time and story text
- Related video embed (YouTube)
- Mobile navigation and a demo newsletter form

## 1. Preview locally
1. Extract the ZIP.
2. Open `index.html` in a browser.
3. For the best local preview, use VS Code's **Live Server** extension.

## 2. Publish on GitHub Pages
1. Sign in at https://github.com and click **New repository**.
2. Name it `newswave` (or another name). Choose **Public** and click **Create repository**.
3. Open the new repository and choose **Add file → Upload files**.
4. Upload **all files and folders inside this ZIP's `newswave-website` folder**. Make sure `index.html` is at the repository root, not inside an extra nested folder.
5. Click **Commit changes**.
6. Open **Settings → Pages**.
7. Under **Build and deployment**, choose **Deploy from a branch**.
8. Select branch **main** and folder **/(root)**, then click **Save**.
9. Wait a minute or two. Your site URL will look like:
   `https://YOUR-USERNAME.github.io/newswave/`

If you name the repository `YOUR-USERNAME.github.io`, the site URL will instead be:
`https://YOUR-USERNAME.github.io/`

## 3. Add or edit news
Open `script.js` and find the `const stories = [...]` list. Each story uses these fields:

```js
{
  id: 10,
  category: "World",
  date: "Nov 18, 2026",
  time: "5 min read",
  title: "Your news headline",
  summary: "A short summary shown on the homepage.",
  image: "https://your-image-url.jpg",
  video: "YOUTUBE_VIDEO_ID",
  author: "Reporter Name",
  body: [
    "First paragraph of your article.",
    "Second paragraph of your article."
  ]
}
```

- `image`: use a direct, publicly accessible image URL (JPG, PNG or WebP).
- `video`: use only the YouTube video ID, not the full URL. For example, for `https://www.youtube.com/watch?v=ysz5S6PUM-U`, the ID is `ysz5S6PUM-U`.
- `date`: enter the actual publication date.
- Add a new story object separated by a comma. Give each story a unique `id`.
- Categories currently used: `World`, `Technology`, `Business`, `Science`, `Culture`.

The sample stories are fictional/demo editorial examples and must not be presented as verified real-world reporting. Replace them with fact-checked articles, licensed images and videos you have permission to publish before launching publicly.

## 4. Important notes
- This is a **static website**. Visitors can read and search news, but there is no admin dashboard, database, automatic news feed or secure editor login.
- The newsletter form is a front-end demo only; it does not save email addresses. Connect a trusted email marketing service if you want subscriptions.
- Images are loaded from Unsplash image URLs and videos from YouTube embeds, so those need an internet connection and may be subject to the providers' terms.
- GitHub Pages hosts the website files; it does not provide a database or server-side code for this project.
