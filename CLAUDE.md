# Esperanto deck

The owner's Esperanto Anki deck, `Languages::Esperanto` in Anki. `build.py` packages every subdeck folder listed in its `PARTS` into `Esperanto.apkg`; `README.md` says what each subdeck holds. Organization rules: the other Anki repos are in `~/organizations/prsnlanki` (GitHub org `prsnlanki`).

1. **Making or changing cards:** read `FLASHCARD_GUIDE.md` in [prsnlanki/anki-setup](https://github.com/prsnlanki/anki-setup) in full first and follow it; check that repo's `backup/exports/all_notes.md` so you don't duplicate existing cards.
2. **Keep note GUIDs stable**, so re-importing updates cards instead of duplicating them.
3. A new kind of card is a new subdeck folder (listed in `build.py`'s `PARTS`), not a new deck. Name decks and subdecks in Anki in the deck's own language, for immersion; folders keep their English names.
4. **Every release** adds a `## x.y.z (date)` section to `CHANGELOG.md` (major when importing needs a step in Anki, minor for new cards, patch for fixes) and points `README.md`'s download link at it; `scripts/check-release-links.sh` (run by `.local-ci`) checks it. After merging, publish from `main` with `scripts/publish.sh`, which builds the `.apkg` and creates the GitHub Release tagged `vx.y.z`.
5. When the deck's notes or description change, update its row in the Decks table of anki-setup's `README.md`.
