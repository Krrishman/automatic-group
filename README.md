# The Automatic Group

Website for The Automatic Group (Long Island, since 1958): one site holding six
division sites, opened by hash routes (`#sprinklers`, `#courts`, `#pools`,
`#landscape`, `#construction`, `#realestate`).

## Run

```
npm install
npm run dev       # Vite dev server
npm run build     # type-check and build to dist/
npm run preview   # serve the build
npm run lint      # oxlint
```

## Where things live

- `src/content.ts` holds every word on the site: the group details, the six
  divisions (names, stats, services, process, questions, contacts) and the
  contact form copy. Edit text here.
- `src/pages/Hub.tsx` is the group page; `src/pages/Division.tsx` renders any
  division from its data.
- `src/ui/` has the top bar, footer, contact form and the count-up numbers.
- `src/scroll/` has Lenis + GSAP smooth scrolling and the reveal / word hooks.
- `src/automatic.css` is the whole stylesheet; design tokens are at the top.
- `public/automatic/photos/` holds the photography; `public/automatic/fonts/`
  the self-hosted Zodiak display font.

## Photos

The current photos are AI-generated placeholders made with
`scripts/generate-automatic-photos.mjs` (Kie.ai, needs `KIE_API_KEY` in the
environment). Replace them with client photography of the same names and
aspect ratios, or edit the paths in `src/content.ts`.

## Deploy

Static output. `npm run build` then upload `dist/` to any static host
(Netlify, Vercel, Cloudflare Pages, S3). No server needed; the contact form
opens a prepared email.
