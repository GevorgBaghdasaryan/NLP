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

W drugim etapie (skrypt ClassicML_NLP_bi) wybrano 3 klasyczne modele - Naive Bayes, Logistic Regression oraz Linear Support Vector Classification. Wytrenowano dane i wyliczono dla każdej predykcji confusion matrix i przygotowano wykres ROC Curve (link 5).

W trzecim etapie (skrypt NN_NLP_bi) zbudowano model Bi-LSTM (Bi-directional long short term memory). Z treningu na 30 epochs wybrano model o największej dokładności i zapisano go do dysku google (link 6) oraz dodano do repozytorium (best_model.hdf5). 


Linki: 
1. Dane źródłowe - id tweetów https://drive.google.com/file/d/1U9FXSMvmtx4e736IvJBWhBldDXif4ZZ0/view?usp=sharing
2. Dane pobrane za pomocą tweepy https://drive.google.com/file/d/147vEMEXvYIhEwBvC_uoh-ZCAUoyBUdXV/view?usp=sharing
3. Wytrenowany model word2Vec https://drive.google.com/file/d/1vmIximvmqTLmAfx-cqSH1EKEX3IQYWOE/view?usp=sharing
4. Dane po preprocessingu https://drive.google.com/file/d/1_dlyuLERXiVH5GFeBBotkadvmpP3bsHs/view?usp=sharing
5. Wyniki etapu 2 - confusion matrix i roc curve https://drive.google.com/drive/folders/1Y4U4Ov4FROjiDM9mhYVmCs6ILnenv6o4?usp=sharing
6. Model bi-LSTM https://drive.google.com/file/d/1xpMzXHPjYH8Vampz3nmpTjhSLUHhUunh/view?usp=sharing
