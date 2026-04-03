# Dutch Learning Anki Deck

## Project
Building an Anki deck from handwritten Dutch lesson notes (photos in `images/`).

## Deck file
- `Nederlands.txt` — Tab-separated Anki import file
- Format: `English/French meaning<TAB>Dutch sentence with <u>word</u> underlined<TAB>tags`
- Header lines: `#separator:tab`, `#html:true`, `#tags column:3`

## Card rules
1. **Front**: For translation cards, front and back must both be full sentences. The front is the English/French sentence, the back is the Dutch sentence. Never put just a word as the front when the back is a sentence. Tag these cards with `sentence`.
2. **Back**: A Dutch sentence using the word, with the target word wrapped in `<u>...</u>`
3. **Tags**: Every card must have at least one tag from: `adverb`, `verb`, `adjective`, `noun`, `pronoun`, `sentence`, `expression`, `question`, `grammar`, `reference`, `family`, `possessive`, `personal`, `preposition`, `color`, or other relevant grammatical category
4. **Dutch correctness**: Always verify Dutch spelling/grammar. Fix any typos from the handwritten notes and flag corrections to the user.
5. **Bilingual user**: The user speaks both English and French. The front of the card can be in either language depending on which was used in the lesson notes.

## Workflow
1. User adds lesson photos to `images/`
2. Claude reads the photos, extracts vocabulary
3. Claude proposes cards with corrected Dutch, flags any typos
4. User validates
5. Claude appends to `Nederlands.txt`
6. Claude commits and pushes to main after every update

## Dutch questions
- When the user asks about a Dutch word or grammar question, always provide the word used in a sentence and include its IPA pronunciation.

## Conventions
- One word/expression per card
- Tags are space-separated in column 3
- Keep existing cards, only append new ones
- Keep this CLAUDE.md up to date when adding new tags or changing conventions
