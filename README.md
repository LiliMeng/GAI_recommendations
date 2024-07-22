# GAI_recommendations

References: https://github.com/WLiK/LLM4Rec-Awesome-Papers

https://github.com/CHIANGEL/Awesome-LLM-for-RecSys
<img width="956" alt="Screenshot 2024-07-22 at 10 03 01 AM" src="https://github.com/user-attachments/assets/b6e98fce-0a57-4321-966f-f014fa1ccbf2">


## Is ChatGPT a Good Recommender? A Preliminary Study

[Paper] (https://arxiv.org/pdf/2304.10149)

<img width="694" alt="Screenshot 2024-07-22 at 10 01 57 AM" src="https://github.com/user-attachments/assets/216d6858-3b87-4878-ab29-0ab98e0d622c">
<img width="1350" alt="Screenshot 2024-07-22 at 10 43 26 AM" src="https://github.com/user-attachments/assets/605a4f32-ed2f-40f1-96bb-4f648a3da481">
<img width="1432" alt="Screenshot 2024-07-22 at 10 43 40 AM" src="https://github.com/user-attachments/assets/287ffaed-7c5d-4dae-818b-b578861d0a16">


Key aspects of the study include:

1. **Task-Specific Prompt Construction**: The authors designed prompts tailored to different recommendation tasks, such as rating prediction and sequential recommendation.
   Each prompt comprises a task description (adapt recommendation tasks to NLP tasks), behavior injection (incorporating user-item interaction, assess the impact of few short learning), and a format indicator to ensure comprehensible outputs.
   

3. **Five Recommendation Scenarios**: The evaluation covers five tasks: rating prediction, sequential recommendation, direct recommendation, explanation generation, and review summarization. The performance is assessed using the Amazon Beauty dataset and human evaluations.

4. **Evaluation and Results**: ChatGPT's performance was benchmarked against traditional methods. The study found that ChatGPT achieved promising results in some tasks and reached baseline levels in others. Human evaluations on explainability-oriented tasks indicated that ChatGPT can generate clearer and more reasonable results, demonstrating its understanding of the provided information. ChatGPT performs well in rating prediction but poorly in sequential and direct recommendation tasks, achieving only similar performance levels to early baseline methods on certain metrics. On the other hand, while ChatGPT demonstrates poor performance in terms of objective evaluation metrics for explainable recommendation tasks such as explanation generation and review summarization, our additional human evaluations show that ChatGPT outperforms state-of-the- art methods. This highlights the limitations of using an objective evaluation approach to accurately reflect ChatGPT’s true explain- able recommendation capabilities. Furthermore, despite ChatGPT’s unsatisfactory performance in accuracy-based recommendation tasks, it is worth noting that ChatGPT has not been specifically trained on any recommendation data. Thus, there is still signifi- cant potential for improvement in future research by incorporating more relevant training data and techniques.

5. **Few-Shot Prompting**: The study also explored the use of few-shot prompting to better capture user preferences and needs, enhancing ChatGPT's ability to make personalized recommendations.

Overall, the study highlights ChatGPT's potential in the recommendation domain, suggesting that with further exploration and refinement, large language models like ChatGPT could significantly improve recommendation systems.
