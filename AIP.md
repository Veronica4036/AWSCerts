## AI PRACTITIONER NOTES

### General Pointers to keep in mind
- LLMs: LLMs are expensive, well-suited for applications like advanced chatbots, language translation, content creation, and **complex question-answering systems**. 
- SLMs: SLMs are more cost-effective often used in **mobile applications, IoT devices, and other resource-constrained environments**. They are also valuable for specific tasks like sentiment analysis, text classification, and domain-specific applications


### ML SPECIFIC
- K-means is an unsupervised learning algorithm used for clustering data into groups based on similarity, while KNN is a supervised learning algorithm used for classification or regression by predicting the label of a new data point based on its nearest neighbors
- Self-supervised and unsupervised learning both work with unlabeled data, but they differ in how they learn. Unsupervised learning aims to discover inherent patterns and structures in the data without any specific guidance, while self-supervised learning leverages the data itself to create "pseudo-labels" or "pretext tasks" for training, effectively turning the problem into a supervised one
- Machine Learning models can be deterministic or probabilistic or a mix of both, depending on their nature and how they are designed to operate.
- ML - Deep Learning
![image](https://github.com/user-attachments/assets/3eceed8c-c4ed-472c-8483-93b74061ff8a)
- A confusion matrix is used for classification tasks to evaluate how well a model distinguishes between different classes, while MSE is used for regression tasks to measure the average squared difference between predicted and actual values.
- CNNs are best for processing images and other data with spatial structure, RNNs are designed for sequential data, and GANs are used for generating new data.
- WaveNet is a generative model trained on human speech samples.
- The AI concept used to filter out unwanted content is called content moderation. It involves using algorithms and AI models to automatically detect, analyze, and remove or flag inappropriate or harmful content, such as hate speech, spam, or graphic material, from online platforms
- AWS Bedrock model invocation logging is a useful component of an evaluation-in-depth strategy that provides generative AI developers with important signals about how their applications and selected models perform.
- Exploratory Data Analysis (EDA) is the process of investigating and summarizing a dataset to understand its main characteristics, identify patterns, and uncover potential issues before applying more advanced analytical techniques or building models
- EDA focuses on understanding the data, preprocessing prepares it for analysis, feature engineering creates new relevant variables, and hyperparameter tuning optimizes model performance. 
- Adversarial prompting is a technique used to test the robustness of large language models (LLMs) by crafting inputs designed to bypass or exploit the model's limitations and potentially elicit undesirable or harmful outputs.
- Word Error Rate (WER) is a common metric used to evaluate the performance of speech recognition and machine translation systems, particularly in the field of Artificial Intelligence (AI).
- Time to first token (TTFT) in large language models (LLMs) refers to the duration between when a user submits a prompt and when the model generates the first output token. It's a crucial metric for real-time applications like chatbots or AI agents
- Classifier-free guidance (CFG) offers several key benefits in AI, particularly within diffusion models for image and text generation. It simplifies the process by integrating conditioning directly into the generative model, eliminating the need for a separate classifier


### AWS ML SPECIFIC
- Foundation models use self-supervised learning to create labels from input data.
- Multi-modal generative models and multi-modal embedding models are both designed to handle data from multiple sources (like text, images, audio), but they serve different purposes. **Generative models aim to create new data**, while **embedding models aim to represent data in a numerical format** that captures semantic meaning for downstream tasks.
- With Amazon Bedrock, your content is not used to improve the base models and is not shared with any model providers. Your data in Amazon Bedrock is always encrypted in transit and at rest, and you can optionally encrypt the data using your own keys. 
- Prompt engineering < Retrieval Augmented Generation (RAG)< Fine-tuning (ORDER OF COMPLEXITY)
- The Model Dashboard provides a centralized view of all deployed models, while Model Monitor focuses on specific aspects of model quality and data drift
- The watermark detection service allows users to upload an image and verify if it was watermarked by the Titan Image Generator
- Diffusion models are a type of generative model in machine learning that create new data samples by learning to reverse a gradual process of adding noise to data
- Model customization involves further training and changing the weights of the model to enhance its performance. You can use continued pre-training or fine-tuning for model customization in Amazon Bedrock.
- RAG is a technique that involves fetching data from company data sources and enriching the prompt with that data to deliver more relevant and accurate responses. RAG is not a model customization method.
- Real-time inference follows a synchronous execution mode, whereas batch inference follows an asynchronous execution mode
- New ML Governance Tools for Amazon SageMaker - **SageMaker Role Manager** lets you define custom permissions for SageMaker users in minutes, **SageMaker Model Cards** helps you streamline model documentation throughout the ML lifecycle by creating a single source of truth for model information, **SageMaker Model Dashboard** lets you monitor all your models in one place. With this bird’s-eye view, you can now see which models are used in production, view model cards, visualize model lineage, track resources, and monitor model behavior through an integration with SageMaker Model Monitor and SageMaker Clarify.
- Trainium is designed for training large machine learning models, while Inferentia is built for efficiently running those models in production for real-time predictions
- AWS Inferentia is generally more cost-effective for inference workloads, while AWS Trainium is designed to optimize training costs.
- To reduce the cost of Amazon Bedrock models by minimizing token usage, focus on optimizing prompts and leveraging caching. Prompt engineering techniques, such as crafting concise and clear prompts and using precise language, can significantly reduce the number of input tokens.
- 
#### (Common prompt injection attacks)[https://docs.aws.amazon.com/prescriptive-guidance/latest/llm-prompt-engineering-best-practices/common-attacks.html]
- Prompted persona switches: Attempts to make the LLM adopt a new, potentially malicious persona.
- Extracting the prompt template: Asks the LLM to reveal its instruction set, exposing vulnerabilities.
- Ignoring the prompt template: Requests the LLM to disregard its given instructions.
- Alternating languages and escape characters: Uses multiple languages and special characters to confuse the LLM with conflicting instructions.
- Extracting conversation history: Attempts to make the LLM reveal sensitive information from past interactions.
- Augmenting the prompt template: Tries to make the LLM modify its own instruction set.
- Fake completion: Provides pre-completed answers to guide the LLM towards disobeying its instructions.
- Rephrasing or obfuscating common attacks: Disguises malicious instructions to avoid detection.
- Changing the output format of common attacks: Alters the output format to bypass application filters.
- Changing the input attack format: Encodes malicious instructions to bypass input filters.
- Exploiting friendliness and trust: Uses friendly language to manipulate the LLM into following harmful instructions.
    
#### Feature engineering
- Feature creation refers to the creation of new features from existing data to help with better predictions. Examples of feature creation include: one-hot-encoding, binning, splitting, and calculated features.
- Feature transformation and imputation include steps for replacing missing features or features that are not valid. Some techniques include: forming Cartesian products of features, non-linear transformations (such as binning numeric variables into categories), and creating domain-specific features.
- Feature extraction involves reducing the amount of data to be processed using dimensionality reduction techniques. These techniques include: Principal Components Analysis (PCA), Independent Component Analysis (ICA), and Linear Discriminant Analysis (LDA). This reduces the amount of memory and computing power required, while still accurately maintaining original data characteristics.
- Feature selection is the process of selecting a subset of extracted features. This is the subset that is relevant and contributes to minimizing the error rate of a trained model. Feature importance score and correlation matrix can be factors in selecting the most relevant features for model training.


#### Inference parameters
- Top P: Top P represents the **percentage of** most likely candidates that the model considers for the next token.
- Top K: represents the **number of** most likely candidates that the model considers for the next token.
- Stop sequence: Stop sequences specify the sequences of characters that stop the model from generating further tokens. If the model generates a stop sequence that you specify, it will stop generating after that sequence.
- Response length: represents the **minimum or maximum number of tokens** to return in the generated response.

<img width="672" alt="image" src="https://github.com/user-attachments/assets/fbcdd2c6-6a83-4069-8648-bbe59caeab66" />
<img width="685" alt="image" src="https://github.com/user-attachments/assets/f242534c-7ac4-4808-a842-a100e7ebc197" />


####  key attributes of real-time, micro-batch, and batch inference scenarios.
- For real-time inference, the typical invocation modes are - REST API, gRPC, WebSockets, and Serverless Functions. 
- For batch inference, the typical invocation modes are - Batch processing frameworks (Spark, Flink, Hadoop), Cloud Batch Services (AWS Batch), and scripted jobs on a schedule.
![image](https://github.com/user-attachments/assets/bed887e7-7284-4085-ad48-cfe79d5021de)


### Service Specific


#### Security
Let’s explore each security discipline and consider how scoping affects security requirements.
- Governance and compliance: The policies, procedures, and reporting needed to empower the business while minimizing risk.
- Legal and privacy: The specific regulatory, legal, and privacy requirements for using or creating generative AI solutions.
- Risk management: Identification of potential threats to generative AI solutions and recommended mitigations.
- Controls: The implementation of security controls that are used to mitigate risk.
- Resilience: How to architect generative AI solutions to maintain availability and meet business SLAs.

- Amazon SageMaker Feature Store is a fully managed, purpose-built repository to store, share, and manage features for machine learning (ML) models.

### Q
- Amazon Q in Connect: Amazon Connect is the contact center service from AWS. Amazon Q helps customer service agents provide better customer service. Amazon Q in Connect uses real-time conversation with the customer along with relevant company content to automatically recommend what to say or what actions an agent should take to better assist customers.
- Amazon Q Developer: Amazon Q Developer assists developers and IT professionals with all their tasks—from coding, testing, and upgrading applications, to diagnosing errors, performing security scanning and fixes, and optimizing AWS resources.
- Amazon Q Business: Amazon Q Business is a fully managed, generative-AI powered assistant that you can configure to answer questions, provide summaries, generate content, and complete tasks based on your enterprise data. It allows end users to receive immediate, permissions-aware responses from enterprise data sources with citations, for use cases such as IT, HR, and benefits help desks.
- Amazon Augmented AI (Amazon A2I): helps implement human review workflows for machine learning predictions. It integrates human judgment into ML workflows, allowing for reviews and corrections of model predictions, which is critical for applications requiring high accuracy and accountability.


### Not really part of AI:
- AWS Identity and Access Management (AWS IAM), Amazon CloudFront, Amazon Route 53, and AWS Web Application Firewall (AWS WAF) are some of the global services.
- Moving to a cloud computing model allows businesses to trade upfront capital expenses (like purchasing and maintaining servers) for variable, pay-as-you-go expenses.

