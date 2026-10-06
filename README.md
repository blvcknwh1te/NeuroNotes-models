# NeuroNotes-models

Released ML assets for [NeuroNotes](https://github.com/blvcknwh1te/NeuroNotes) — an on-device Flutter notes app.

## Contents

Releases in this repository carry the sentence-embedding model used for local semantic search:

| File | Purpose |
|---|---|
| 
ote_embedding.tflite | Encoder: text -> 384-dim L2-normalized vector (int8 weights, float32 activations) |
| 	okenizer.json | Matching HuggingFace tokenizer (padding/truncation to 128 tokens) |
| manifest.json | modelVersion, sizes and sha256 checksums |

The model and the tokenizer are a matched pair: they must always be downloaded from the same release tag.

## Source

Base model: sentence-transformers/paraphrase-multilingual-MiniLM-L12-v2 (Apache-2.0).
Export pipeline lives in the main repository: 	ool/export_embedding_model.py.