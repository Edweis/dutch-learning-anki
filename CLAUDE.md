# Dutch Learning Anki Deck

## Project
Building an Anki deck from handwritten Dutch lesson notes (photos in `images/`).

## Deck file
- `Nederlands.txt` — Tab-separated Anki import file
- Format: `English/French meaning<TAB>Dutch sentence with <u>word</u> underlined<TAB>tags`
- Header lines: `#separator:tab`, `#html:true`, `#tags column:3`

## Card rules
1. **Front**: English or French meaning of the word
2. **Back**: A Dutch sentence using the word, with the target word wrapped in `<u>...</u>`
3. **Tags**: Every card must have at least one tag from: `adverb`, `verb`, `adjective`, `noun`, `pronoun`, `sentence`, `expression`, `question`, `grammar`, `reference`, `family`, `possessive`, `personal`, or other relevant grammatical category
4. **Dutch correctness**: Always verify Dutch spelling/grammar. Fix any typos from the handwritten notes and flag corrections to the user.
5. **Bilingual user**: The user speaks both English and French. The front of the card can be in either language depending on which was used in the lesson notes.

## Workflow
1. User adds lesson photos to `images/`
2. Claude reads the photos, extracts vocabulary
3. Claude proposes cards with corrected Dutch, flags any typos
4. User validates
5. Claude appends to `Nederlands.txt`

## Conventions
- One word/expression per card
- Tags are space-separated in column 3
- Keep existing cards, only append new ones
- Keep this CLAUDE.md up to date when adding new tags or changing conventions
