## Projekt analizy sentymentu NLP
### ZUM - semestr zimowy 2021/22
Analizowano tweety w języku polskim na temat epidemii COVID. Dane źródłowe zawierające jedynie id tweetów pobrano z https://doi.org/10.5281/zenodo.3723939. Ponieważ dane oraz wytrenowane modele mają powyżej 25 MB poniżej umiesciłęm linki do dysku Google. 

W pierwszym etapie (skrypt Preprocessing_NLP_bi):
  1. Pobrano dane po id używając funkcji statuses_lookup z tweepy (link 2). 
  2. Dane wyczyszczono, znormalizowano, usunięto stopwords oraz stokenizowano.
  3. Zainicjowano i wytenowano model word2Vec - word embedding (link 3). 
  4. Za pomocą Kmeans podzielono dane na 2 klastry - pozytywny oraz negatywny. 
  5. Ręcznie poprawiono skład klastrów.
  6. Zmapowano sentymenty do danych za pomocą funkcji get_sentiments i zwizualizowano rozkład sentymentów w tweetach.
  7. Dane po preprocessingu zapisano jako tweets_labeled_bi.csv (link 4) 

![image](https://user-images.githubusercontent.com/81071435/147371241-d77e96d3-4d68-4ce5-b3ec-209d96a23f25.png)

W drugim etapie (skrypt ClassicML_NLP_bi) wybrano 3 klasyczne modele - Naive Bayes, Logistic Regression oraz Linear Support Vector Classification. Wytrenowano dane i wyliczono dla każdej predykcji confusion matrix i przygotowano wykres ROC Curve.
![LR](https://user-images.githubusercontent.com/81071435/147371340-6ea3f7de-b8a5-4b67-8b3b-8d12546f0a13.PNG)

![NB](https://user-images.githubusercontent.com/81071435/147371346-c40619eb-1d32-4bd9-afd8-ad3454d9e690.png)





Linki: 
1. Dane źródłowe - id tweetów https://drive.google.com/file/d/1U9FXSMvmtx4e736IvJBWhBldDXif4ZZ0/view?usp=sharing
2. Dane pobrane za pomocą tweepy https://drive.google.com/file/d/147vEMEXvYIhEwBvC_uoh-ZCAUoyBUdXV/view?usp=sharing
3. Wytrenowany model word2Vec https://drive.google.com/file/d/1vmIximvmqTLmAfx-cqSH1EKEX3IQYWOE/view?usp=sharing
4. Dane po preprocessingu https://drive.google.com/file/d/1_dlyuLERXiVH5GFeBBotkadvmpP3bsHs/view?usp=sharing
