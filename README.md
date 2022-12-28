# NLP
# TEXT CLASSIFICATION
The objective was to explore different text classification models using different feature extraction techniques.
Inspect the results and choose the champion model then do further analysis to understand why the champion model was performing well on the collected books partitions corpus.
Fivebooks in the detective and mystery storiescategorywere selected to create the text partitionsthat will be used throughoutthe assignment.
Different combinations of feature extraction techniquesand classification modelswere used.The selected champion model was Naïve Bais classifier using BOW–with max_df equal 30 to and ngrams_range equal to (1,2)-and TF-IDFfor feature extraction. 
The error analysis of the champion model showed that the model was performing well because it was using the character names found in the books. 
Also, the stemmed partitionsand lemmatized partitions were used to measure their effect on the model’s accuracy but they had little to no effect on the accuracy.
A group of five books were selected from Gutenberglibrary, each book had a different author but all of them fall under detective and mystery stories category,
the labels are used to identifythe books partitionsthroughout the analysis and modeling.
![image](https://user-images.githubusercontent.com/121487638/209854274-7a66fa6f-fd9f-43f1-883e-99e03c8efe28.png)
Preprocessing and Data Cleansing:
The following steps were followedto transform the raw data into useful and efficient format.
1.The books were downloaded from Gutenberg online library, the extra padding added by Gutenburg library which included copyrights information was removed and only the book text was retrieved.
2.The book’s sentences were tokenized using nltk word tokenizer.
3.Stop words and punctuation markswere removed,so that modelscan focus on unique information that can be used for classification.
4.The first 100 words were skipped to avoid getting cover page, table of contents, and introduction chapter text in the selected books partitions which would not have helped 
in classifying the book. It is an important step at data cleaning because they are unnecessary or useful input for the model and can affect the performance.
5.200 book partitions were acquired from all the books, each books partitions had a unique label and all of the partitions were added to a dataframe to facilitate further processing, 
the books partitions were shuffled to avoid model classifying using books partitions sequential index.
