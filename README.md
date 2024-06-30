# llm-context-caching
This project implements Gemini's "context caching" functionality on for the Llama3 series of models. For many chat interface services, a user (and sometimes multiple users) will ask prompts over the same set of documents. Tokenizing and rerunning the same documents through the LLM is costly and significantly reduces the Time to First Token (TFT) from a user's perspective. Here, we precompute the KV caches for a redundant set of documents and load them into memory before the first prompt is fired.

This is a demo repo for the Llama3 and CUDA ecosystems and is not currently compatible with Metal Performance Shaders or other GPU backends. Please contact the project admin if you would like to implement this for your project or company.