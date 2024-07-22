# GAI_recommendations

References: https://github.com/WLiK/LLM4Rec-Awesome-Papers

https://github.com/CHIANGEL/Awesome-LLM-for-RecSys
<img width="956" alt="Screenshot 2024-07-22 at 10 03 01 AM" src="https://github.com/user-attachments/assets/b6e98fce-0a57-4321-966f-f014fa1ccbf2">

## Generate Rather Than Retrieve: Large Language Models Are Strong Context Generators

full paper [here](https://openreview.net/forum?id=fB0hRu9GZUS).

This work leverages large language models (LLMs) to generate contextual documents for knowledge-intensive tasks such as open-domain question answering (QA), fact-checking, and dialogue systems. This approach contrasts with traditional methods that rely on retrieving relevant documents from external sources before generating answers.

### Key Points:

1. **GenRead Pipeline**:
   - **Generate-Then-Read Approach**: Instead of retrieving documents, GenRead first prompts a large language model to generate relevant contextual documents based on the given question. Then, it reads these generated documents to produce the final answer.
   - **Zero-Shot Setting**: In the zero-shot setting, the model generates contextual documents without any training data. This method significantly outperforms traditional retrieve-then-read pipelines by leveraging the LLM's ability to generate context-specific information directly.

2. **Clustering-Based Prompting**:
   - To improve the diversity and recall of the generated documents, the authors propose a clustering-based prompting method. This method selects distinct prompts from different clusters of question-document pairs to generate documents covering various perspectives. This approach enhances the overall quality and relevance of the generated content.

3. **Performance and Evaluation**:
   - **Experiments**: GenRead achieves impressive results on several benchmarks. For instance, it obtains exact match scores of 71.6 on TriviaQA and 54.4 on WebQ, outperforming state-of-the-art retrieve-then-read systems by significant margins.
   - **Combination with Retrieval**: The paper also suggests that combining retrieval and generation can further improve performance, indicating that these methods can be complementary.

4. **Challenges and Solutions**:
   - **Document Diversity**: Generating multiple high-quality documents is challenging. The authors address this by using diverse human prompts and clustering-based methods to ensure a broad coverage of knowledge and reduce repetitiveness in generated texts.

### Conclusion
The GenRead method highlights the potential of large language models to serve as powerful context generators, offering a promising alternative to traditional document retrieval methods for knowledge-intensive tasks. This approach can lead to more accurate and contextually relevant answers by directly leveraging the vast knowledge encoded in LLMs.


## Actions Speak Louder than Words: Trillion-Parameter Sequential Transducers for Generative Recommendations (from Meta ICLM2024)

full paper [here](https://openreview.net/forum?id=xye7iNsgXn)

The paper introduces a new architecture for recommendation systems called the Hierarchical Sequential Transduction Unit (HSTU). This model is designed to handle the high cardinality, non-stationary nature of streaming recommendation data using generative modeling frameworks.

### Key Contributions:

1. **Generative Training Approach**:
   - The authors propose moving from traditional impression-level training to a generative training framework, significantly reducing computational complexity. This approach amortizes encoder costs across multiple targets, making the training process more efficient and scalable for industrial-scale systems.

2. **Hierarchical Sequential Transduction Unit (HSTU)**:
   - HSTU is composed of layers connected by residual connections and includes sub-layers for Pointwise Projection, Spatial Aggregation, and Pointwise Transformation. This design replaces heterogeneous modules in traditional deep learning recommendation models (DLRMs) with a single modular block, simplifying and enhancing the model's efficiency.

3. **Performance and Efficiency**:
   - HSTU-based Generative Recommenders outperform traditional models on various datasets, showing improvements of up to 65.8% in Normalized Discounted Cumulative Gain (NDCG) and being 5.3x to 15.2x faster than FlashAttention2-based Transformers on sequences of length 8192. The model has been deployed on a large internet platform with billions of users, demonstrating its practical scalability and efficiency.

4. **Scalability and Carbon Footprint**:
   - The model's performance scales as a power-law of training compute, similar to other large-scale models like GPT-3 and LLaMa-2. This scaling reduces the carbon footprint required for future developments and paves the way for creating foundation models in the recommendation domain.

The paper highlights the potential of using large-scale generative models in recommendation systems, offering significant improvements in performance and efficiency over traditional methods.


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

Overall, the experimental results show that ChatGPT performs well in rating prediction but poorly in sequential and direct recommendation tasks, indicating the need for further exploration and improvement. Despite its limitations, ChatGPT outperforms state-of-the-art methods in terms of human evaluation for explainable recommendation tasks, highlighting its potential to generate explanations and summaries. 

### Top-k Hit Ratio (HR@k) for Sequential and Direct Recommendation

**Definition:**
- **Hit Ratio (HR@k)** is a metric used to evaluate the effectiveness of a recommender system by checking if the true positive item (the item that a user actually interacted with) appears in the top-k recommended items.

**Calculation:**
- For each user, if the true positive item is within the top-k items recommended by the system, it is considered a hit.
- HR@k is then calculated as the ratio of the number of hits to the total number of users.

<img width="689" alt="Screenshot 2024-07-22 at 11 20 26 AM" src="https://github.com/user-attachments/assets/f62545eb-6de9-433d-9818-c688f0ad5438">


**Use in Sequential Recommendation:**
- In sequential recommendation, HR@k measures how well the system predicts the next item a user will interact with, considering the order and context of previous interactions.

**Use in Direct Recommendation:**
- For direct recommendation, HR@k evaluates the overall ability of the system to recommend relevant items from a static set of candidate items.

### Top-k Normalized Discounted Cumulative Gain (NDCG@k) for Sequential and Direct Recommendation

**Definition:**
- **Normalized Discounted Cumulative Gain (NDCG@k)** is a metric that measures the ranking quality of the recommended items, taking into account the position of the true positive items in the recommended list and the relevance of the recommendations.

**Calculation:**
- **DCG@k (Discounted Cumulative Gain):** For each user, calculate the cumulative gain of the recommended items up to position \(k\), with gains discounted logarithmically based on the position of the items.

<img width="725" alt="Screenshot 2024-07-22 at 11 20 36 AM" src="https://github.com/user-attachments/assets/8a6d1208-621d-455e-8864-632561a5d06a">


**Use in Sequential Recommendation:**
- In sequential recommendation, NDCG@k evaluates the system's ability to rank the next items in a sequence in an order that reflects the user's actual preferences, considering the sequence and context of prior interactions.

**Use in Direct Recommendation:**
- For direct recommendation, NDCG@k assesses the ranking quality of a set of recommended items, ensuring that more relevant items (those the user interacts with or rates highly) are ranked higher in the list.

### Summary of Use Cases

1. **Sequential Recommendation:**
   - **HR@k:** Measures whether the next item in a user's interaction sequence appears in the top-k recommendations.
   - **NDCG@k:** Evaluates how well the recommender system ranks the next item in terms of relevance and position in the top-k list.

2. **Direct Recommendation:**
   - **HR@k:** Checks if any relevant item is in the top-k recommended items for a user.
   - **NDCG@k:** Assesses the overall ranking quality of recommended items, ensuring that highly relevant items are given higher priority in the recommendation list.

These metrics are crucial in evaluating the performance of recommender systems, providing insights into both the accuracy (HR@k) and the ranking quality (NDCG@k) of the recommendations.
