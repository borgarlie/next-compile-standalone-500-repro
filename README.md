# next compile mode + standalone: missing /500 chunks

```
npm install
npm run build   # next build --experimental-build-mode compile
npm start       # node .next/standalone/server.js
```

Open http://localhost:3000/?fail=1. The custom 500 page fails with a
`ChunkLoadError`, because its chunk is in `.next/server` but not in
`.next/standalone`. A normal `next build` shows the custom 500 page.
