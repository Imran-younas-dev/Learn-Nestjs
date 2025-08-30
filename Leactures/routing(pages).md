#### <a> vs <link>

In Next.js, using a normal <a> tag for internal links causes a full page reload, breaking the single-page app experience. To fix this, you should use the Link component from next/link, which keeps navigation fast, seamless, and client-side, while still using server-rendered content under the hood. This gives you the best of both worlds: server-rendered first load + smooth SPA navigation.

#### Working with Pages & Layouts

In Next.js, `page.js` defines the **page content**, while `layout.js` defines the **wrapper (shell)** around one or more pages.

- Every project needs at least **one root `layout.js`**.
- You can also create **nested layouts** for specific folders.
- The `children` prop is used to inject the active page into the layout.
- `layout.js` sets up the **HTML skeleton** (like `<html>` and `<body>`), while metadata (title, description, etc.) is handled via a special exported **`metadata` object**, not a `<head>` tag.

👉 In short: `layout.js` = structure/wrapper, `page.js` = actual page content.
