# DonkeyCut light and dark review evidence

Screenshots for the draft dark-mode PR against DonkeyCut/Donkey. This branch holds review evidence and is separate from the application change.

- `current-notes/`: 22 final captures from commit `914efb1ef0a710e6eadbd5b52e877259ade4bdd2`. Five stored paper colors in both themes, paper/text menus, selection, mobile sheet, and explicit overrides. Dark named/default text samples reached at least 5.86:1. This is sample verification, not full accessibility certification.
- `earlier-review/`: 94 captures from `14c073ba96e7dd7e602c05e7f38634435eb89fa6`. The 21-route review reached expected fixture content for 40/42 light/dark combinations; the shared viewer stayed loading in both. Earlier bright yellow dark-note captures are superseded by current-notes.
- `historical-archive/`: all 48 requested original captures, unchanged. These belong to the older patch based on `29d420e` and are historical evidence, not current verification.

Captures use anonymous local fixtures and public media, with isolated Chrome contexts. OCR/GPS checks found no credential-like text or GPS metadata. Login/authorization screenshots and raw OCR are excluded. SHA-256 hashes are listed in `manifest.json`.

The final focused tests passed 23/23. Production compilation and TypeScript passed; complete prerender failed without the required DB/auth configuration. Full lint retains two independently confirmed upstream errors. The earlier aggregate suite reported 4,758 pass, 4 skip, 2 fail, 1 error; the two affected files subsequently passed 16 tests. The entire suite was not rerun. Real persistence, purchases, generation/export, native Mac/OPFS, mobile editor, and every data/error state remain unverified.
