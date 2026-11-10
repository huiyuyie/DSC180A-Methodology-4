# DSC 180A Methodology Assignment 4

**Name:** Huiyu Yie

**UCSD Email:** huyie@ucsd.edu

**Section:** D12

**Mentor:** Goutham Valeti

## Reflection Questions

**1. What is the most interesting topic covered in your domain this quarter?**  
What I found most interesting this quarter was how we could combine AI-assisted labeling with human review to build a more efficient transaction categorization pipeline.
In our domain, our main goal is to use NLP techniques to categorize bank transactions based on their memo descriptions, so we can better understand people's financial behavior and use this information for credit risk analysis.
Since we're working with a huge amount of transaction data, manually labeling every transaction would take too much time. 
Using LLMs can help us generate labels much faster, but we also found that these labels were not always accurate, especially when the memo descriptions were unclear or could fit into multiple categories. 
During our manual review process, I noticed that we sometimes had to look up the company names mentioned in the memos to understand what the businesses actually do and decide which category a transaction most likely belonged to. 
But knowing the company name still did not always tell us exactly what the consumer purchased. This motivates me to explore how RAG could help retrieve relevant business information and provide more context for categorizing ambiguous transactions. 
I also found it interesting how we could use these labels to train a FastText model, which turns out to be a more efficient way to classify transactions comparing to using TF-IDF.
Overall, it was interesting to see how the combination of AI and human judgment can work together to make the pipeline more efficient and reliable. 

**2. Describe a potential investigation you would like to pursue for your Quarter 2 Project.**  
One potential investigation for our Quarter 2 project would be to explore whether spending and income-related features from bank transactions could help us predict signs of financial stress and assess consumers' creditworthiness.
In our current Quarter 1 project, we are focusing on using NLP to categorize bank transactions and extract useful spending and income-related features. 
Building upon this, we could look into whether gasoline spending patterns, including spending amounts, purchase frequency, and consistency, could help identify signs of financial stress when combined with income levels and income stability.
Since the same amount of gasoline spending could take up a different portion of income for different consumers, I believe considering these features together could provide more useful information. 
I would also compare predictive models using separate training, validation, and test sets to see how well they could predict indicators of financial stress and which features are most useful for evaluating credit risk. I could also examine how the efficiency and accuracy of our AI labeling process could affect the quality of these features and model performance. 

**3. What is a potential change you'd make to the approach taken in your current Quarter 1 Project?**  
During our experiments, we found that some transactions could fit into multiple categories, and different reviewers sometimes assigned different labels to the same transaction. So one change I would make is to improve the quality and consistency of our labeled data before training and tuning the FastText model. Starting with our regex-based labeling approach, I would consider refining some of our existing rules and creating more specific subcategories for broader categories. Some of our current categories may be too general to capture the differences between certain types of transactions. 
I would also consider building a knowledge base of company information and previously reviewed transactions, which could be used with RAG to provide more context when labeling unclear or unfamiliar transaction memos. So that our labeling process can be more consistent and reliable while reducing the amount of manual research needed. 

**4. What other techniques would you be interested in using in your project?**  
I would be interested in exploring agentic AI programming to help us develop and improve our data processing and model training pipeline. For example, we could use AI coding agents to help us integrate everyone's work into a single pipeline in our team's GitHub repository, automate repetitive tasks, and test different modeling approaches, while still reviewing and verifying the process and results ourselves. 
I would also like to try BERT for transaction categorization and compare its performance with our current FastText model. Since BERT can better capture the context of words, I think it would be interesting to see whether it could improve classification accuracy, especially for ambiguous transaction descriptions.
For our Q2 project, I would also be interested in using XGBoost to analyze whether combining gasoline spending patterns and income-related features could help identify signs of financial stress. 
