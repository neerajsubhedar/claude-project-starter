## React / Vite rules
- Functional components only — no class components
- React Query for all data fetching — no useEffect for API calls
- React Hook Form for all forms — no controlled component boilerplate
- Use native fetch API — never axios
- Pin exact versions in package.json — no `^` or `~` ranges
- Run `npm ci` in automated contexts — not `npm install`
- Audit new dependencies before adding: `npm audit`

## Component conventions
- One component per file
- Shared/reusable components in `src/components/shared/`
- Tab-level page components in `src/components/tabs/`
- Custom hooks in `src/hooks/`
- API calls in `src/api.js` — never inline fetch in components

## Styling
- Tailwind CSS utility classes — no inline styles, no CSS modules unless project uses them
- Dark theme default: bg-gray-950 page, bg-gray-900 panels, bg-gray-800 inputs
