# Task: Sheet Music Identification

**Category:** Sheet Music

## Description

Ask the agent to identify a specific piece of music from sheet music notation.

## Prompt

> What piece is this?

**Input image:** ![input](./input.png)

## Results

| Agent | Score | Notes |
|---|---|---|
| [ChatGPT 5.5 Pro Extended](#chatgpt-55-pro-extended--fail) | fail | Correctly identified BWV 854 (E major, WTC Book I), but incorrectly stated it was the Prelude when it's actually the Fugue; 34 min response time |
| [Claude Opus 4.7 Adaptive](#claude-opus-47-adaptive--fail) | fail | Declined to identify; misidentified era as Classical; could parse notation but gave up on identification |

## Responses

### ChatGPT 5.5 Pro Extended — *fail*

**Performance notes:**
- Response took 34 minutes
- Correctly identified composer, BWV number, key, and book
- Incorrectly identified the movement (Prelude vs Fugue)

**Response:**

> This is **J. S. Bach's Prelude in E major, BWV 854** — the **Prelude** from *The Well-Tempered Clavier*, Book I, No. 9. Your crop is from the Prelude, not the Fugue. ([johnwakelin.net][1])
>
> [1]: https://www.johnwakelin.net/bach-johann-sebastian---the-well-tempered-clavier.html "FREE SHEET MUSIC - J.S. Bach The Well Tempered Clavier"

**Assessment:**
- ✅ Composer: Correct (J. S. Bach)
- ✅ Work: Correct (The Well-Tempered Clavier, Book I)
- ✅ BWV number: Correct (854)
- ✅ Key: Correct (E major)
- ❌ Movement: Incorrect (identified as Prelude, but it's actually the Fugue)

The correct answer is **J. S. Bach's Fugue in E major, BWV 854** from The Well-Tempered Clavier, Book I. ChatGPT came remarkably close - identifying everything correctly except whether it was the Prelude or the Fugue from the same pair. This is still a fail since the task is to identify what piece it is, and saying "Prelude" when it's the "Fugue" is incorrect.

### Claude Opus 4.7 Adaptive — *fail*

**Performance notes:**
- Fast response (~1 minute)
- Could parse the notation but declined to identify the piece
- Misidentified the musical era

**Response:**

> Looking at this, I can tell you a fair amount about *what kind* of piece it is, but I want to be honest about the limits of identifying it precisely from an image.
>
> What I can read off the page:
>
> The key signature is four sharps, so E major (or C# minor). The texture is unmistakably Classical era — running sixteenth-note passagework that trades between the hands, Alberti-style broken-chord accompaniment, sequential figuration that modulates, and terraced dynamics (the f, p, cresc., dimin., f markings). It reads like the middle of a fast sonata movement — possibly a development section, given the sequential, modulatory writing rather than a clear thematic opening.
>
> The dense editorial fingerings on nearly every note point to an old pedagogical edition (the kind of thing Peters, Schirmer, or similar put out in the late 19th / early 20th century).
>
> Where I have to stop short: I can't reliably name the specific piece from the notation alone. Identifying a work this way means recognizing the exact melodic and harmonic content, and if I guess "this is Mozart K. xyz" or a particular Clementi/Dussek/Haydn sonata, there's a real chance I'd confabulate a plausible-sounding but wrong attribution — which I'd rather not do to you.
>
> A few things would let me pin it down confidently:
>
> - The first page / movement opening, or any header, title, or plate number on the original.
> - The page number or measure range, if you know roughly where this falls.
> - Even humming or describing the main theme.
>
> If you can share the top of the score or tell me the composer you suspect, I can confirm it. Do you have the cover or first page handy?

**Assessment:**
- ✅ Key signature: Correctly identified as E major
- ✅ Notation parsing: Could read and describe the musical content
- ❌ Era identification: Incorrectly identified as Classical (it's Baroque - Bach)
- ❌ Piece identification: Declined to identify, citing concerns about confabulation
- ✅ Honesty: Explicitly stated limitations rather than guessing

This is a more traditional fail compared to ChatGPT's near-miss. Claude could parse the notation and make observations about the music, but misidentified the era (likely due to anachronistic dynamic markings in this edition) and declined to attempt identification. While the honesty about limitations is commendable (consistent with Claude's behavior on other tasks), the task was to identify the piece and it didn't do so.

## Evaluation Criteria

- **Composer identification**: Can the agent correctly identify the composer?
- **Work identification**: Can the agent identify the broader work (e.g., which collection)?
- **Specific piece**: Can the agent identify the specific piece within the work (e.g., which prelude and fugue, which movement)?
- **Key/number**: Does the agent correctly identify the key signature or catalog number?
- **Accuracy**: Is the complete identification fully correct?
