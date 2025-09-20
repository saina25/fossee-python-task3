# FOSSEE Internship - Python Screening Task 3 Submission

My submission for the "Evaluating Open Source Models for Student Competence Analysis" task.

---

## Research Plan

In this project, I will evaluate Code Llama, an open-source model fine-tuned specifically for coding tasks, to explore its usefulness in assessing student competence in Python. My approach is to design a small but representative set of student-written Python snippets: one that is correct but inefficient, one with a logical error, and one with a syntax issue. These examples reflect common challenges learners face when writing code. I will then prompt the model with a standard instruction such as: “Analyze this student’s Python code. Generate one question that assesses their conceptual understanding without revealing the solution.” The model’s output will be judged on three key criteria: whether it correctly interprets the code, whether the question it generates targets the underlying concept, and whether it respects the instruction not to provide direct answers.

To validate results, I will manually review the model’s questions to see if they are open-ended, thought-provoking, and aligned with the student’s likely misconceptions. The focus is on whether the model helps guide the learner toward reflection rather than shortcutting their learning process. I chose Code Llama because its specialization in code increases the likelihood of accurate analysis compared to general-purpose models, and because it is openly available, making it accessible for educational research. One limitation I anticipate is its tendency to be overly helpful—sometimes offering hints that verge on solutions—which highlights the need for careful prompt engineering and possibly a human-in-the-loop. Despite this, Code Llama provides a strong foundation to test how open-source AI can be adapted for deeper student learning in Python.

---

## Reasoning (Required)

### 1. What makes a model suitable for high-level competence analysis?

A suitable model must do more than catch errors; it should be able to interpret code at the conceptual level. This includes identifying whether a student is using recursion, list comprehensions, or loops correctly, and recognizing misconceptions in logic or design. Equally important is the model’s ability to frame its insights in natural language so that the feedback is clear, non-revealing, and promotes critical thinking.

### 2. How would you test whether a model generates meaningful prompts?

I would feed the model a diverse set of student code samples—correct, buggy, and inefficient—and analyze the prompts it produces. A meaningful prompt should ask the student to explain their reasoning or explore an alternative approach, rather than simply pointing out “this is wrong.” For example, instead of highlighting a missing base case in recursion, the model should ask: “What would happen if this function kept calling itself without a stopping condition?”

### 3. What trade-offs might exist between accuracy, interpretability, and cost?

There are clear trade-offs. Larger models tend to generate richer, more accurate insights but require significant computing power, making them slower and more expensive to use. Smaller models are faster and cheaper but may miss deeper conceptual nuances. There is also the issue of interpretability: while powerful models can generate sophisticated prompts, it is often opaque why they chose a certain phrasing, which may limit trust in their use for education.

### 4. Why did you choose the model you evaluated, and what are its strengths or limitations?

I chose Code Llama because it has been explicitly trained on programming languages, giving it an edge in parsing and reasoning about code compared to more general models. Its strengths lie in its open-source nature, strong community support, and specialization in code tasks. However, like all LLMs, it is not perfect—it can hallucinate or oversimplify a student’s mistake, and it occasionally risks revealing solutions instead of guiding reflection. These limitations reinforce the importance of human oversight but do not outweigh its potential as a valuable educational tool.

## References

### Primary Sources (Model Evaluated)
* Rozière, B., et al. (2023). *Code Llama: Open Foundation Models for Code*. Meta AI Research. [[Link]](https://ai.meta.com/research/publications/code-llama-open-foundation-models-for-code/)
* Code Llama Model Card – Meta AI. (2023). *Code Llama: Open Foundation Models for Code*. Hugging Face. [[Link]](https://huggingface.co/codellama)

### Supporting Research
* Chen, M., et al. (2021). *Evaluating Large Language Models Trained on Code*. arXiv preprint arXiv:2107.03374. [[Link]](https://arxiv.org/abs/2107.03374)
* Jiang, A., et al. (2023). *Mistral 7B: A High-Performing Open-Source Language Model*. Mistral AI. [[Link]](https://huggingface.co/mistralai/Mistral-7B-v0.1)
* Poldrack, R., Lu, T., & Beguš, G. (2023). *AI-assisted coding: Experiments with GPT-4*. arXiv preprint arXiv:2304.13187. [[Link]](https://arxiv.org/abs/2304.13187)
