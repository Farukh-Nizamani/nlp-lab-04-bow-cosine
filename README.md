# Natural Language Processing Assignment


### Task 1 -- Bag of Words construction
<img width="1114" height="569" alt="image" src="https://github.com/user-attachments/assets/3904dabb-2892-49ac-a5d0-e967791c7a33" />


<img width="1115" height="401" alt="image" src="https://github.com/user-attachments/assets/5437c47d-8a39-4a85-bdd3-b1b88bfc4ab8" />


### Task 2 -- Document Search Engine & Relevance Ranking
<img width="1105" height="592" alt="image" src="https://github.com/user-attachments/assets/55804de8-695f-412b-b0cb-464493528b88" />


<img width="1116" height="242" alt="image" src="https://github.com/user-attachments/assets/a3b29b11-fa44-473f-b11d-5a33afcdd871" />


## Questions & Answers
###### Question 1:
**Why does the sentence "Dog bites man" have the exact same Bag of Words representation as "Man bites dog"? How does this impact sentiment analysis?**


**answer**: Bag of Words disregards the order of words and focuses only on how often each word appears. Therefore, both “Dog bites man” and “Man bites dog” are represented in exactly the same way: [dog:1, bites:1, man:1]



###### Question 2:
**What happens to the memory size and density of the BoW matrix when the corpus contains 100,000 unique vocabulary words?**


**answer**: If the vocabulary contains 100,000 unique words, the BoW matrix will have 100,000 columns. For N documents, its size becomes:
> N * 100,000


###### Question 3:
**Explain why Document 3 in Task 2 receives a Cosine Similarity score of 0.0000 when queried against "machine learning algorithms for data"**

**answer**:
Document 3 contains the sentence:

> "Natural language processing helps computers understand human language"

The query is:

> "machine learning algorithms for data"

Once CountVectorizer converts them into vectors, Document 3 and the query have no words in common. As a result, their vector dot product is zero:

> q · d₃ = 0

Consequently, their cosine similarity is also zero:

> cos(q, d₃) = 0.0000

Therefore, based on the Bag of Words representation, the search engine considers Document 3 completely unrelated to the query.






