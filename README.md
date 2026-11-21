# biharilm

Building language technology for the Bihari languages, starting with **Bhojpuri**, then **Maithili** and **Magahi**.

Bhojpuri alone has around 50 million speakers in India (2011 census), plus communities in Nepal, Mauritius, Fiji and the Caribbean. Yet most AI models handle it poorly: it is often folded into Hindi, there is little clean text online, and very few ways to measure how well a model understands it.

This project works through the whole stack, one phase at a time, in the open.

## Roadmap

| Phase | What | Status |
|---|---|---|
| 1 | **Tokenizer audit.** How much more does the same sentence cost in Bhojpuri than in English or Hindi, across today's major models? | in progress |
| 2 | **Dataset.** Collect, clean and publish an openly licensed Bhojpuri text corpus. | planned |
| 3 | **Evaluation set.** Questions and tasks to measure how well any model understands Bhojpuri. | planned |
| 4 | **A tiny model from scratch.** Train a small GPT style model on the corpus to understand every piece of the pipeline. | planned |
| 5 | **Fine tuning.** Adapt an open model to Bhojpuri with LoRA and compare it against the base model on the eval set. | planned |
| 6 | **Demo.** A public chat demo on Hugging Face Spaces. | planned |
| 7 | **Look inside.** An interactive tool to visualise what the model learned: attention, embeddings, and how Bhojpuri relates to Hindi inside the model. | planned |

Maithili and Magahi join from phase 2 onwards.

## Structure

```
phase1_tokenizer_audit/   measuring tokenizer cost across languages
```

Each phase gets its own folder with its own notes, code and results.

## Building on

This project stands on earlier work, especially:

- [FLORES+](https://huggingface.co/datasets/openlanguagedata/flores_plus): the same 2,000+ sentences professionally translated into 200+ languages, including Bhojpuri, Maithili, Magahi and Hindi (CC BY-SA 4.0)
- [AI4Bharat](https://huggingface.co/ai4bharat): open datasets and models for Indian languages
- Research on Bhojpuri, Maithili and Magahi part of speech tagging, named entities, and MaiBERT for Maithili

## About

Made by [Anubhuti Raj](https://github.com/rajanubhuti), a designer from Bihar learning how language models work by building one for home.
