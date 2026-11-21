# Phase 1: Tokenizer audit

## The question

Language models read text as **tokens**: small chunks, sometimes a whole word, sometimes a few letters. Models are priced, limited and slowed down by token count.

If a model's tokenizer was built mostly on English, a Bhojpuri sentence gets chopped into many more pieces than the same sentence in English. That means it costs more, fits less into the model's memory, and is usually understood worse.

**How big is that "token tax" for Bhojpuri, Maithili and Magahi, compared with Hindi and English, across today's major models?**

## Data

FLORES+ (dev split): the same sentences translated into:

| Language | Code |
|---|---|
| English | `eng_Latn` |
| Hindi | `hin_Deva` |
| Bhojpuri | `bho_Deva` |
| Maithili | `mai_Deva` |
| Magahi | `mag_Deva` |

Because the sentences mean the same thing in every language, any difference in token count comes from the tokenizer, not the content.

## Tokenizers to compare

- OpenAI (`o200k_base`, used by GPT 4o and later), through `tiktoken`
- Llama 3
- Gemma
- Qwen
- An Indian model's tokenizer (for example Sarvam or AI4Bharat), as a comparison point

Some of these need a free Hugging Face account, and some models ask you to accept their terms on their page before you can download the tokenizer.

## What to measure

- **Tokens per sentence** for each language and tokenizer
- **Fertility:** tokens per word. Close to 1 is good, much higher means words are being shredded
- **Token tax:** tokens in language X divided by tokens in English for the same sentence
- **Characters per token:** how much text each token carries

## Steps

1. Set up a Python environment and install `datasets`, `tiktoken`, `transformers`, `pandas`, `matplotlib`
2. Load FLORES+ for the five languages and check a few sentences look right
3. Write a function that counts tokens for one sentence with one tokenizer
4. Run every sentence through every tokenizer and save the results to `results/tokens.csv`
5. Calculate the measures above and make charts
6. Look at a few real examples of how a Bhojpuri word gets split, since these make the finding feel real
7. Write up what you found in `FINDINGS.md`: the numbers, the charts, and what they mean

## What you'll learn

How tokenizers work (BPE and SentencePiece), loading datasets from Hugging Face, working with pandas, and turning analysis into clear charts.

## Status

Not started.
