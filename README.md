# GAI_recommendations

Papers: https://github.com/WLiK/LLM4Rec-Awesome-Papers

https://github.com/CHIANGEL/Awesome-LLM-for-RecSys

## Is ChatGPT a Good Recommender? A Preliminary Study

[Paper] (https://arxiv.org/pdf/2304.10149)

Key aspects of the study include:

1. **Task-Specific Prompt Construction**: The authors designed prompts tailored to different recommendation tasks, such as rating prediction and sequential recommendation. Each prompt comprises a task description, behavior injection (incorporating user-item interaction), and a format indicator to ensure comprehensible outputs.

2. **Five Recommendation Scenarios**: The evaluation covers five tasks: rating prediction, sequential recommendation, direct recommendation, explanation generation, and review summarization. The performance is assessed using the Amazon Beauty dataset and human evaluations.

3. **Evaluation and Results**: ChatGPT's performance was benchmarked against traditional methods. The study found that ChatGPT achieved promising results in some tasks and reached baseline levels in others. Human evaluations on explainability-oriented tasks indicated that ChatGPT can generate clearer and more reasonable results, demonstrating its understanding of the provided information. ChatGPT performs well in rating prediction but poorly in sequential and direct recommendation tasks, achieving only similar performance levels to early baseline methods on certain metrics. On the other hand, while ChatGPT demonstrates poor performance in terms of objective evaluation metrics for explainable recommendation tasks such as explanation generation and review summarization, our additional human evaluations show that ChatGPT outperforms state-of-the- art methods.

4. **Few-Shot Prompting**: The study also explored the use of few-shot prompting to better capture user preferences and needs, enhancing ChatGPT's ability to make personalized recommendations.

Overall, the study highlights ChatGPT's potential in the recommendation domain, suggesting that with further exploration and refinement, large language models like ChatGPT could significantly improve recommendation systems.
