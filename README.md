**Face Emotion Recognition App**

aplikacija prepoznaje emocije u stvarnom vremenu preko web kamere. model je treniran u pytorch-u kroz cnn arhitekturu, dok opencv sluzi za detekciju lica na video streamu.

kod i pokretanje se nalaze u `FaceEmotionRecognitionApp.ipynb`, a grafovi u `training_curves.png` i `confusion_matrix.png`.

projekt je baziran na [youtube tutorialu](https://www.youtube.com/watch?v=snnEtCiDeiE&list=LL&index=5) i [kaggle datasetu](https://www.kaggle.com/datasets/fahadullaha/facial-emotion-recognition-dataset), ali uz par izmjena da se poboljsa tocnost.

### sto je promjenjeno u odnosu na tutorial:

    * rezolucija slika: zadrzano je originalnih 96x96 piksela (u tutorialu je smanjeno na 64x64).
    * dublja mreža: dodan je 5. cnn sloj (sa 512 filtara) za bolje izvlacenje znacajki.
    * duze treniranje: broj epoha je podignut na 70 uz dodan early stopping.

### rezultati i overfitting:

ove promjene su podigle tocnost sa **63.9%** (iz tutoriala) na **76.1%**.

*napomena:* na grafu 'training_curves.png' se vidi overfitting vec nakon 21. epohe. tu val_loss prestaje padati, dok train_acc nastavlja rasti do 85%.
