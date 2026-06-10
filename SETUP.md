# Publishing this profile

GitHub shows a README on your profile page when it lives in a repository
**named exactly like your account** — for you that's `tjark-neumann/tjark-neumann`.

## Steps

1. Create a new **public** repository called `tjark-neumann`
   (GitHub will show a "✨ special repository" banner — that's the one).
2. Copy `README.md` and the whole `assets/` folder into it, keeping the structure:

   ```
   tjark-neumann/
   ├── README.md
   └── assets/
       ├── header-light.svg
       ├── header-dark.svg
       ├── ticker.svg
       ├── divider.svg
       └── surfboard.stl   (optional — it's already embedded in the README)
   ```

3. Commit and push. Your profile at github.com/tjark-neumann updates immediately.

## Notes

- The header switches automatically between the sunset (light) and dusk (dark)
  variant via `<picture>` + `prefers-color-scheme`.
- All animations are CSS keyframes *inside* the SVGs — GitHub strips CSS from
  markdown but plays it inside images, which is why this works.
- The 3D surfboard and the map render natively from the `stl` / `geojson`
  code blocks. Drag the surfboard to rotate it.
- Everything respects `prefers-reduced-motion`, so it degrades gracefully.
- Want different ticker words? Edit the two `<text>` lines in
  `assets/ticker.svg` — keep both lines identical so the loop stays seamless.
