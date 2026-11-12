
# Experiment 01: Basic LLM Chatbot

## Objective

Build a basic conversational AI application using a pretrained Large Language Model (LLM) and understand the fundamental components involved in LLM inference.

## Environment

| Component | Selection |
|---|---|
| Model | Qwen2.5-0.5B-Instruct |
| Framework | Hugging Face Transformers |
| Deep learning framework | PyTorch |
| Language | Python |


## Implementation

The chatbot implements the following workflow:

1. Load a pretrained tokenizer and model.
2. Accept a user question.
3. Format messages using the model's chat template.
4. Convert the formatted prompt into tokens.
5. Run model inference.
6. Decode generated tokens into readable text.
7. Store user and assistant messages in conversation history.
8. Include previous messages when processing subsequent questions.

## Concepts Explored

### Model loading
Loaded an instruction-tuned Qwen model using Hugging Face Transformers.

### Tokenization
Explored how natural language is converted into token IDs before inference.

### Text generation
Used autoregressive generation to predict subsequent tokens.

### Prompt engineering
Compared different system instructions and observed how they influenced response style.

### Chat templates
Used structured system, user, and assistant messages.

### Conversation memory
Implemented application-managed conversation history using a Python list.

### Hardware acceleration
Configured Google Colab to use GPU acceleration when available.

## Observations

- Different system prompts can influence response style and structure.
- Fluent responses are not necessarily factually correct.
- Conversation history allows the application to provide previous context to the model.
- Increasing conversation history increases the input token count.
- Model inference performance depends on hardware and generation settings.

## Limitations

- The model does not have access to live networking information.
- The model can generate inaccurate technical explanations.
- Conversation history is stored in application memory and is not persistent across runtime restarts.
- No external networking documentation or RAG pipeline is implemented yet.
- No formal response-quality evaluation has been implemented.

## Future Improvements

1. Benchmark CPU and GPU inference performance.
2. Measure token generation throughput and latency.
3. Implement context-window management.
4. Add automated tests.
5. Add networking documentation retrieval using RAG.
6. Introduce response-quality evaluation.

## Learning Outcome

Developed a foundational understanding of LLM loading, tokenization, prompting, inference, and application-managed conversation context.
