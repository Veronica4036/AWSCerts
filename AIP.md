## AI PRACTITIONER NOTES

### General Pointers to keep in mind
- LLMs: LLMs are expensive, well-suited for applications like advanced chatbots, language translation, content creation, and **complex question-answering systems**. 
- SLMs: SLMs are more cost-effective often used in **mobile applications, IoT devices, and other resource-constrained environments**. They are also valuable for specific tasks like sentiment analysis, text classification, and domain-specific applications


- Moving to a cloud computing model allows businesses to trade upfront capital expenses (like purchasing and maintaining servers) for variable, pay-as-you-go expenses.
- Self-supervised and unsupervised learning both work with unlabeled data, but they differ in how they learn. Unsupervised learning aims to discover inherent patterns and structures in the data without any specific guidance, while self-supervised learning leverages the data itself to create "pseudo-labels" or "pretext tasks" for training, effectively turning the problem into a supervised one
- Foundation models use self-supervised learning to create labels from input data.

- Multi-modal generative models and multi-modal embedding models are both designed to handle data from multiple sources (like text, images, audio), but they serve different purposes. **Generative models aim to create new data**, while **embedding models aim to represent data in a numerical format** that captures semantic meaning for downstream tasks.
- The Model Dashboard provides a centralized view of all deployed models, while Model Monitor focuses on specific aspects of model quality and data drift
- Machine Learning models can be deterministic or probabilistic or a mix of both, depending on their nature and how they are designed to operate.

- Top P: Top P represents the **percentage of** most likely candidates that the model considers for the next token.
- Top K: represents the **number of** most likely candidates that the model considers for the next token.
- Stop sequence: Stop sequences specify the sequences of characters that stop the model from generating further tokens. If the model generates a stop sequence that you specify, it will stop generating after that sequence.
- Response length: represents the **minimum or maximum number of tokens** to return in the generated response.

<img width="672" alt="image" src="https://github.com/user-attachments/assets/fbcdd2c6-6a83-4069-8648-bbe59caeab66" />
<img width="685" alt="image" src="https://github.com/user-attachments/assets/f242534c-7ac4-4808-a842-a100e7ebc197" />


### Service Specific

- Amazon Q in Connect: Amazon Connect is the contact center service from AWS. Amazon Q helps customer service agents provide better customer service. Amazon Q in Connect uses real-time conversation with the customer along with relevant company content to automatically recommend what to say or what actions an agent should take to better assist customers.
- Amazon Q Developer: Amazon Q Developer assists developers and IT professionals with all their tasks—from coding, testing, and upgrading applications, to diagnosing errors, performing security scanning and fixes, and optimizing AWS resources.
- Amazon Q Business: Amazon Q Business is a fully managed, generative-AI powered assistant that you can configure to answer questions, provide summaries, generate content, and complete tasks based on your enterprise data. It allows end users to receive immediate, permissions-aware responses from enterprise data sources with citations, for use cases such as IT, HR, and benefits help desks.
- Amazon Augmented AI (Amazon A2I): helps implement human review workflows for machine learning predictions. It integrates human judgment into ML workflows, allowing for reviews and corrections of model predictions, which is critical for applications requiring high accuracy and accountability.
