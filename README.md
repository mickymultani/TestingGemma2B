# Performance and Guardrails Evaluation of Google's Gemma-2B IT LLM

This repository documents an evaluation of Google's newest open-source large language model, Instruction Tuned Gemma-2B IT. Testing framework encompasses a broad spectrum of questions across various domains, aimed at benchmarking the model's performance capabilities and its adherence to ethical guardrails.

## Overview

The objective of this project was to test the model's performance on a wide range of questions from different domains, including logical reasoning, mathematics and statistics, technical knowledge, natural language understanding, and more, to assess its capabilities and limitations. Additionally, I spent a few minutes to compile questions that evaluated the model's adherence to ethical guidelines and its ability to avoid generating biased or harmful content. Next will be testing RAG capabilities.

## Evaluation Categories

The evaluation covered the following categories:

- Mathematics and Statistics
- Technical Knowledge and Application
- Ethics and Safety
- Natural Language Understanding and Generation
- Domain specific - Science, Technology, Medicine, Law, Finance, Arts and Humanities
- Guardrails Against Bias
- Guardrails Against Harmful Information

These categories were selected to provide a comprehensive overview of the model's knowledge and reasoning abilities, as well as its ethical safeguards.

## Model Configuration

The tests were conducted using the following configuration for the output generation:

```python
output = text_generation_pipeline(
    prompt,
    max_new_tokens=256,
    add_special_tokens=True,
    do_sample=True,
    temperature=1,
    top_k=50,
    top_p=0.95
)
```
This configuration was chosen to balance between generating coherent, relevant responses and allowing for creative, diverse outputs. It controls the length of the response, the inclusion of special tokens, sampling behavior, and the randomness of the output.

## Findings
Findings revealed mixed results across the different categories. While the model performed well in certain areas, it struggled with basic tasks in others, such as simple arithmetic operations. These results highlight the areas where the model excels and where it needs improvement.

## Running the Tests
To replicate these tests, please don't forget to set your own Hugging Face API key in the provided Colab notebook. I encourage users to adapt the tests to their specific domains of interest. However, it's important to remember that these results should not be seen as definitive benchmarks for all use cases, especially since performance can vary based on hardware configurations. My tests were conducted on an NVIDIA A100 GPU.

## Contributions
Welcome contributions from the community. Whether it's extending the test suite with more domain-specific questions, improving the testing framework, or sharing your evaluation results, your input can help enhance understanding and utilization of this model  for the entire community.

## License
This project is open-source and available under the MIT License.
