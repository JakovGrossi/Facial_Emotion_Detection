Aplikacija za preoznavanje emoicija preko web kamere.

Ovaj projekt je aplikacija za prepoznavanje emocija u stvarnom vremenu preko web kamere. Model je treniran u PyTorch-u (CNN arhitektura), a za detekciju lica na videu koristi se OpenCV.

Projekt je rađen prema YouTube tutorialu (https://www.youtube.com/watch?v=snnEtCiDeiE&list=LL&index=5) i dataset sa Kaggle-a (https://www.kaggle.com/datasets/fahadullaha/facial-emotion-recognition-dataset), ali uz nekoliko izmjena koje su poboljšale rezultat.
Što je promijenjeno u odnosu na tutorial

    Veličina slika: Zadržana je originalna rezolucija od 96x96 piksela, dok je u tutorialu smanjena na 64x64.

    Arhitektura mreže: Iskoršten je dublji model s 5 CNN slojeva.

    Treniranje: Broj epoha je povećan na 70 uz uključen Early Stopping.

Rezultati i Overfitting

Zahvaljujući ovim promjenama, model je postigao bolju točnost na validacijskom skupu:

    Točnost u tutorialu: 63.9%

    Moja točnost: 76.1%

Napomena o treniranju

Iako je konačni rezultat bolji, na grafu training_curves.png jasno se vidi overfitting nakon 25. epohe. Gubitak na validaciji tu prestaje padati i lagano raste, dok točnost na trening skupu nastavlja rasti prema gore.

Pokretanje se vidi u datoteci FaceEmotionRecognitionApp.ipynb, dok su grafovi performansi spremljeni u datotekama training_curves.png i confusion_matrix.png.
