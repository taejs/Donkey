# Current review evidence — 2026-10-26

Application revision: `55c748d678337fb90eca64477d9878e140f30a79`. These are 29 fresh PNG captures from the actual Next.js application in isolated Chrome contexts at 1920×1080, with system light/dark emulation. No user browser profile or production data was used.

Requested system-dark review states:

1. **Notes grid and open note: verified.** All five paper colors have light/dark captures. Each pair of full open-note PNGs is byte-identical (see `note-comparison.json`). Paper, text color, label and formatting menus were also inspected in both themes.
2. **Timeline and inspector: verified with fixtures.** Two video tracks, a title track and an audio track; decoded public starter media, selected video and selected title with their inspectors.
3. **Conversation with a tool-call card: verified with fixtures.** Persisted sample conversation and expanded `add_title` result; no model request or tool execution.
4. **Loaded shared project: blocked.** Both direct navigation and a Next Link from fixture blog content reach the shared editor's loading state, with `projectId=review`, `readOnly=true`, `loaded=false`, `loadError=null`; no shared document request follows the successful meta request. `shared-blocked-dark.png` is failure evidence, not a loaded-view capture. The production cause is not established.

Additional inspected states: Library with a note and loaded public poster; landing hero and scrolled navigation in both themes. The current head's only change from `2e05a4a` is the landing mock's white dark border. The dark donkey artwork stays on a white rounded tile.

Current-head validation: 94 related tests passed, 0 failed, 497 assertions (11 files, 1.82s); TypeScript noEmit passed; ESLint on the newly changed EditorMock.tsx passed. The full suite and production build were not rerun for this revision. GitHub's Site analytics tests and DonkeyKit tests passed at this head.

The QA server substitutes anonymous API/session/project/note/chat/blog data and a no-database Prisma shim; it does not replace UI components, hooks or theme CSS. Media comes from committed public starter files through fixture URLs, so real signed R2 delivery is unverified. Server mutations are blocked; the editor's “Couldn't save” badge is expected fixture behavior, not a persistence check. Browser storage is an isolated temporary context. Real authentication, permissions, persistence, mobile editor, generation/export and payments were not exercised. This is sample QA, not full page/state or accessibility certification.

All PNGs were visually inspected (identical light-note pixels checked by hashes), scanned with offline OCR and checked for GPS metadata. No credential-like text, private filesystem paths or GPS metadata was found. Raw OCR, logs and auth screens are not published. Production config is restored after QA.

Older image collections remain unchanged historical evidence; their dark note tints and backlit mark are superseded by the maintainer's current design.
