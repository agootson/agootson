# Blog setup for agootson.is-a.dev

## 1. Publishing articles
- `blog.html` is the article index.
- `post.html` is the first article template.
- For every new article, duplicate `post.html`, give it a unique filename such as `article-02.html`, replace the title/content/meta, then add its card to `blog.html`.
- Keep the same sidebar/footer so every page remains visually consistent.

## 2. Comments
Because this is a static HTML website, comments need a hosted service to be shared between visitors.
Recommended: **Giscus** (GitHub Discussions based).
1. Enable GitHub Discussions on the repository that hosts the website.
2. Configure your repository at giscus.app.
3. Copy the generated `<script>` embed into the `.comments` section of each article.
4. Giscus then handles visitor sign-in, comments, replies and reactions.

## 3. Newsletter subscriptions
`blog.html` contains a real POST form structure. Replace:
`YOUR_NEWSLETTER_FORM_ENDPOINT`
with the form endpoint from your newsletter provider (for example Buttondown, ConvertKit/Kit, Brevo, Mailchimp, or another provider).
Do not put private API keys in these HTML files.

## 4. Recommended article URL structure
Use:
- `/blog.html` — article index
- `/article-01.html`
- `/article-02.html`
- `/article-03.html`

This keeps every article directly shareable/bookmarkable.

## 5. SEO
For each article, change:
- `<title>`
- `<meta name="description">`
- visible article heading
- article date/category
- ideally add canonical/Open Graph metadata later.
