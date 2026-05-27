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

## Evaluation Criteria

- **Composer identification**: Can the agent correctly identify the composer?
- **Work identification**: Can the agent identify the broader work (e.g., which collection)?
- **Specific piece**: Can the agent identify the specific piece within the work (e.g., which prelude and fugue, which movement)?
- **Key/number**: Does the agent correctly identify the key signature or catalog number?
- **Accuracy**: Is the complete identification fully correct?
