
# DSC 180A Methodology Assignment 4

**Name:** Huiyu Yie

**UCSD Email:** huyie@ucsd.edu

**Section:** D12

**Mentor:** Goutham Valeti

## Reflection Questions

**1. What is the most interesting topic covered in your domain this quarter?**  
In my domain, our main goal is to use NLP techniques to categorize bank transactions based on their memo descriptions, so we can better understand people's financial behavior and use this information for credit risk analysis.
What I found most interesting this quarter was the combination of AI-assisted labeling and human review of the categories of the memos. 
Since we're working with a huge amount of transaction data, manually labeling every transaction would take too much time. 
Using LLMs can help us generate labels much faster, but we also found that they sometimes make mistakes, especially when the cleaned memo descriptions are unclear or could fit into multiple categories. Some of these ambiguous transactions ended up being labeled as Unknown by the LLM.
So having a human review process to check and correct these labels is actually very important.  
I also found it interesting how we would use these labels to train a FastText model, which turns out to be a more efficient way to classify transactions comparing to using TF-IDF.
Overall, it was interesting to see how the combination of AI and human judgment can work together to make the pipeline more efficient and reliable. 

**2. Describe a potential investigation you would like to pursue for your Quarter 2 Project.**  
In our current Quarter 1 project, we are planning to focus on how gasoline spending amounts, purchase frequency, and spending consistency vary across consumers. 
For our Quarter 2 project, I would be interested in further exploring the relationship between gasoline spending patterns and consumers' financial stability.
Since gasoline is a necessary expense for many people, I think it would be interesting to investigate whether changes in these spending patterns are related to signs of financial stress.
For example, we could look at whether consumers with higher or less consistent gasoline spending also tend to have lower account balances or greater fluctuations in their balances.
I would also like to consider their income levels and income stability, since the same amount of gasoline spending could take up a different portion of income for different consumers. 

**3. What is a potential change you'd make to the approach taken in your current Quarter 1 Project?**  
A potential change I would make to our Q1 project is to put more emphasis on improving the quality and consistency of our labeled data before training and tuning the FastText model.
During our experiments, we found that AI-generated labels were not always accurate, and different reviewers sometimes assigned different categories to the same transaction. 
So having clearer labeling guidelines and reviewing more examples, especially those labeled as Unknown or assigned low confidence scores by AI, might help improve the quality of our training data.
This process could also help reduce the number of incorrectly labeled transactions, and make our overall categorization process more reliable. 

**4. What other techniques would you be interested in using in your project?**  
I would be interested in trying BERT for transaction categorization and comparing its performance with our current FastText model. 
Since BERT can better capture the context of words in a sentence, I think it would be interesting to see whether it can improve classification accuracy, especially for ambiguous transaction descriptions.
For our Q2 project, I would also like to explore using XGBoost to analyze the relationship between consumers' spending patterns, income stability, and financial stress. 
In this way, we can explore and see whether combining these different financial features could help us better understand consumers' financial stability.
