```
npx create-next-app@latest
```

```
npm run dev
```

Hydration is the process by which React transforms static HTML generated on the server into an interactive application on the client.

Server component x Client component
    ^
(default behavior)

To create a route, create a folder with a page.jsx file inside it. Add subfolders to add sublinks

Layout file is for navbar, footer, etc. Content that will repeat on all the pages

Insteat of using <a> tag, use <Link>
```
import Link from 'next/link'

<Link href="/">Text</Link>
```