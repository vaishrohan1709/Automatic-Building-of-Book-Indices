
CSE 519 -- Data Science (Fall 2017)
Project Progress Report
Kiranmayi Kasarapu - 111447596
Shruti Nair - 111481332
Rohan Vaish - 111447435

Project: Automatic Building of Book Indices

Challenge
The goal of our project is to predict the indices for a journal or article given in the form of latex file. We have to build index based on the content of the article and write indices back to the latex source file.
BaseLine Model
Frequency Based Index Building
For the baseline model, we implemented the frequency search algorithm shown above to extract the most frequently occurring words in the document. Based on the number of indices, the user inputs, say n, we extracted the top n frequently occurring words and listed them out as the indices for the document.
	
Algorithm:
Have a large corpus of text against which we can compare.
Tag each tokenizer according to its type after removing all the stop words.
Find the relative frequency of words in the corpus. For example, if your corpus is "the green way is very green way green". Relative frequency is.. [ (the, 1/8), (green, 3/8), (way, 2/8), (is, 1/8), (very, 1/8), ]
Get the relative frequency of words in search string.
Divide frequency of search string by corpus, and also take care of the cases, when the word is not included in the string.
Sort the answer by the result obtained in d and generate the top n words as given by the user.
The below graph shows the number of matched indices percentage in 4 different files. 
