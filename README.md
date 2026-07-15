Explainable RAG Pipeline
┌──────────────────────┐
│    User Question     │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│   Query Processing   │
│ • Tokenization       │
│ • Stopword Removal   │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│   TF-IDF Retriever   │
│ • Vectorization      │
│ • Cosine Similarity  │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│ Document Ranking     │
│ • Similarity Score   │
│ • Top-K Selection    │
└───────┬───────┬──────┘
        │       │
        │       │
        ▼       ▼
 Retrieved   Rejected
Documents   Documents
        │
        ▼
┌──────────────────────┐
│ Context Construction │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│    Claude Sonnet     │
│      LLM Engine      │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│  Generated Answer    │
└──────────┬───────────┘
           │
           ▼
┌────────────────────────────────────┐
│ Explainability Layer               │
│                                    │
│ • Confidence Score                 │
│ • Hallucination Probability        │
│ • Claim-Level Grounding            │
│ • Retrieved Document Evidence      │
│ • Rejected Document Explanation    │
│ • Reasoning Path                   │
└──────────┬─────────────────────────┘
           │
           ▼
┌──────────────────────┐
│ Interactive Dashboard│
└──────────────────────┘
```
