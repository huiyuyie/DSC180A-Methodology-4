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
During our manual review process, I noticed that we sometimes had to look up the company names mentioned in the memos to understand what the business actually do, and decide which category a transaction most likely belongs to. 
But knowing the company name still did not always tell us exactly what the consumer purchased. 
I also found it interesting how we would use these labels to train a FastText model, which turns out to be a more efficient way to classify transactions comparing to using TF-IDF.
Overall, it was interesting to see how the combination of AI and human judgment can work together to make the pipeline more efficient and reliable. 

**2. Describe a potential investigation you would like to pursue for your Quarter 2 Project.**  
In our current Quarter 1 project, we are planning to focus on how gasoline spending amounts, purchase frequency, and spending consistency vary across consumers. 
For our Quarter 2 project, I would be interested in further exploring the relationship between gasoline spending patterns and consumers' financial stability.
Since gasoline is a necessary expense for many people, I think it would be interesting to investigate whether changes in these spending patterns are related to signs of financial stress.
For example, we could look at whether consumers with higher or less consistent gasoline spending also tend to have lower account balances.
I would also like to consider their income levels and income stability, since the same amount of gasoline spending could take up a different portion of income for different consumers. 

**3. What is a potential change you'd make to the approach taken in your current Quarter 1 Project?**  
A potential change I would make to our Q1 project is to put more emphasis on improving the quality and consistency of our labeled data before training and tuning the FastText model.
During our experiments, we found that AI-generated labels were not always accurate, and different reviewers sometimes assigned different categories to the same transaction. 
So having clearer labeling guidelines and reviewing more examples, especially those labeled as Unknown or assigned low confidence scores by AI, might help improve the quality of our training data.
This process could also help reduce the number of incorrectly labeled transactions, and make our overall categorization process more reliable. 

**4. What other techniques would you be interested in using in your project?**  
I would be interested in exploring agentic AI programming to help us develop and improve our data processing and model training pipeline. For example, we could use AI coding agents to help us combine our work into a clear pipeline, automate repetitive tasks, and test different modeling approaches, while still reviewing and verifying the process and results ourselves. 
I would also like to try BERT for transaction categorization and comparing its performance with our current FastText model, especially for ambiguous transaction descriptions.
For our Q2 project, I would also be interested in using XGBoost to analyze whether combining gasoline spending patterns and income-related features could help identify signs of financial stress. 
