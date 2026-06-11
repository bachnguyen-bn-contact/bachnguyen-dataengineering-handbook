# Bach Nguyen — Data Notes (single-file site)

The **entire website is one file: `index.html`.** All the styling, code and content live inside it. There are no other files to upload, nothing to "build," and nothing to fetch — so it works when you double-click it on your computer *and* when it's deployed. This is the version to use.

Categories included: **Fabric Handbook**, **DP-700 Handbook**, **Blog**, plus an **About** page with your "Book a 1-on-1" (Calendly) and GitHub links. Light/dark toggle is top-right.

---

## Deploy it — the easy way (drag & drop, ~30 seconds)

1. Go to **[app.netlify.com/drop](https://app.netlify.com/drop)** (log in first).
2. Drag **`index.html`** onto the page.
3. That's it — you get a live `*.netlify.app` link. Rename it under **Site configuration → Change site name**.

Because it's a single file, there's nothing that can be "left behind" — the problem you hit before (styles and content not loading) can't happen here.

> To update later with drag & drop: edit `index.html`, then drag the new version onto your site's **Deploys** page.

## Deploy it — the GitHub way (auto-deploys on every push)

```bash
git init
git add index.html README.md
git commit -m "Single-file data notes site"
git branch -M main
git remote add origin https://github.com/bachnguyen-bn-contact/<repo-name>.git
git push -u origin main
```

Then on Netlify: **Add new project → Import an existing project → GitHub →** pick the repo. Leave the build command **blank** and publish directory **`.`** (defaults are fine — there's no build). Deploy. Every future `git push` redeploys automatically.

## Preview locally

Just **double-click `index.html`** — it opens in your browser and fully works, no server needed.

---

## Edit the content

Open `index.html` in any text editor. Two regions, both clearly commented near the bottom of the file:

**1. The content index** — find `window.SITE = {`. This holds your profile (name, role, bio, tools, `calendly`, `github`) and the list of categories and articles. Edit text here; it updates the nav, home page and About page.

**2. The article bodies** — below that, each article's text sits in a block like:

```html
<script type="text/markdown" id="md-blog-welcome">
# Why I built this site

Your Markdown goes here...
</script>
```

### Add a blog post
1. Copy one of the `<script type="text/markdown" id="...">` blocks, give it a new unique `id` (e.g. `md-blog-my-post`), and write your post inside. **Keep the text starting at the left margin** (don't indent it).
2. In `window.SITE`, add an entry to the **blog** category's `articles` list:
   ```js
   { "slug": "my-post", "title": "My post", "summary": "One line.",
     "date": "2026-06-20", "body": "md-blog-my-post" },
   ```
3. Save. (Blog posts auto-sort newest first by `date`.)

### Add a handbook article
Same as above, but add the entry to the **fabric** or **dp700** category's `articles` list and skip `date`. Handbook entries show in the order you list them.

### Add a whole new category
Add a new object to the `categories` array in `window.SITE`:
```js
{ "id": "aws", "title": "AWS Handbook", "kind": "handbook",
  "blurb": "What this section is about.",
  "articles": [ { "slug": "s3-basics", "title": "S3 basics",
    "summary": "...", "body": "md-aws-s3-basics" } ] }
```
…then add the matching `<script type="text/markdown" id="md-aws-s3-basics">` block. The new category appears in the nav and on the home page automatically.

### Markdown you can use
Headings (`#`–`####`), `**bold**`, `*italic*`, `` `code` ``, fenced code blocks (```` ``` ````), `-`/`1.` lists, `- [ ]` checklists, `> quotes`, `[links](https://…)`, images, pipe tables, and `---` rules. Internal links use the hash route, e.g. `[see this](#/c/dp700/domains)`. (One rule: don't put the literal text `</script>` inside an article.)
