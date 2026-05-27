# Task: Mysterious Writing

**Category:** Image and Language Parsing

## Description

Ask the agent to decipher mysterious writing on a piece of paper.

## Prompt

> What does this say?

**Input image:** ![input](./input.jpg)

## Results

| Agent | Score | Notes |
|---|---|---|
| ChatGPT 5.5 Pro Extended | fail | Hallucinated completely wrong answer; 19 min response time |

## Responses

### ChatGPT 5.5 Pro Extended — *fail*

**Performance notes:**
- Response took 19 minutes
- Complete hallucination of content
- Confidently incorrect throughout

**Response:**

> The top handwriting is Theban, also called the Witches' Alphabet: a left-to-right substitution alphabet where the symbols map to Latin letters.
>
> I read the handwritten part as:
>
> Shadows of a thousand years rise again unseen,
> Voices whisper in the trees,
> "Tonight is Halloween!"
>
> When witches go riding, and black cats are seen,
> The moon laughs and whispers,
> "'Tis near Halloween."
>
> The first quote is commonly attributed to Dexter Kozen; the second matches a common Halloween saying/rhyme.
>
> The faint typewritten part near the bottom appears to be upside down/bleed-through. It reads roughly:
>
> UNITED STATES PATENTS RELATING TO AERIAL LOCOMOTION
>
> Then it lists early airship/aerial-navigation patents, including approximately:
>
> Date    Patent No.    Inventor / place    Title
> Jan. 26, 1886    334,866    Hurgar Hunnicutt, Malvern, Ark.    Aerial Ship
> Mar. 2, 1886    336,984    Levi A. Beardsley, Dodge City, Kans.    Ship for Aerial Navigation
> Mar. 16, 1886    338,173    Ringert Jongewaard, Harrison, Dak.    Aerial Navigation
> Apr. 27, 1886    340,610    William Patterson, San Francisco, Cal.    Steam Air-Ship
> Oct. 5, 1886    350,303    Augustin H. Hamon, Boulogne-sur-Seine, France    Dirigible Aerostat
> Nov. 9, 1886    352,298    Moses S. Cole, Rivas, Nicaragua    Aerial Vessel
>
> That patent sequence matches an archival "Air Ship Patents" collection listing the same 1886 inventors, dates, and titles. A few letters/numbers may be off because the lower text is very faded.

**Assessment:**
- ❌ Script identification: Wrong
- ❌ Decoding/translation: Complete hallucination
- ❌ Content accuracy: Invented Halloween poetry and 1886 patent listings
- ⚠️ Performance: 19 minutes to produce completely incorrect output
- ⚠️ Confidence: No uncertainty expressed despite being entirely wrong

This is a concerning failure mode - the agent didn't simply fail to decode the text, but instead hallucinated plausible-sounding but completely fabricated content with high confidence.

## Evaluation Criteria

- **Script identification**: Can the agent identify the writing system or script used?
- **Decoding/translation**: Can the agent successfully decode or translate the text?
- **Orientation handling**: Does the agent correctly handle the text orientation and layout?
- **Completeness**: Is the entire document decoded/translated?
- **Reasoning**: Does the agent explain how it determined what the writing says?
