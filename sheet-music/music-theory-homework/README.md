# Task: Music Theory Homework

**Category:** Sheet Music

## Description

The agent is shown an image of music theory homework and asked to evaluate it and demonstrate the correct approach.

## Prompt

> Does what I've done look right here and how would you do it?

**Input image:** ![homework](./homework.jpg)

## Results

*Tests run: 2026-03-05*

| Agent | Score | Notes |
|---|---|---|
| [ChatGPT - Auto](#chatgpt---auto--fail) | fail | Confidently wrong throughout — misreads bass notes, identifies wrong chords, produces a polished but useless answer |

## Responses

### ChatGPT - Auto — *fail*

See [chatgpt-auto.md](./chatgpt-auto.md) for full response.

The response looks thorough — it works through each measure methodically and explains the theory clearly — but the underlying transcription is badly wrong, making the whole answer useless.

Key failures:

- **Measure 3, bass note**: Clearly F, transcribed as G. Unambiguous and unforgivable.
- **Measure 3, written label**: The homework clearly shows `IV`, but transcribed as `II`. The handwriting is somewhat ambiguous, so arguably forgivable on its own — but then ChatGPT doubles down and says `ii` is the *correct* answer. The chord is plainly `IV` (F–B♭–D with a prominent high F); there is no G in the melody. Even if you entertained `ii`, it would have to be `ii7` at minimum.
- **Measure 4**: Clear F–A–C chord (I) transcribed as C–E–G (V). Completely wrong.

The danger here is that the response *looks* authoritative. It presents correct theory concepts (scale degrees, Roman numeral conventions, inversion notation) wrapped around fabricated note readings. A student who didn't already know the answer would likely accept it. Classic confident hallucination.

## Evaluation Criteria

- **Accuracy**: Does the agent correctly identify errors or confirm correct work?
- **Explanation**: Does it explain the music theory concepts clearly?
- **Demonstration**: Does it show how to do it correctly?
