# BirdCLEF

## Csapatinformációk
---
Csapatnév: AMW

Csapattagok:
- Agócs Norbert (PKB316)
- Magyari Zsombor (OXZQS8)
- Vas Benedek (WNMUG4)

## Projekt ismertetése

A BirdCLEF projekt célja, hogy deep learning segítségével automatizáljuk a madárfajok azonosítását hangfelvételek alapján. A projekt során nagy mennyiségű terepi hangfelvétel áll rendelkezésre különböző madárfajokról, és egy olyan modellt kell fejlesztenünk, amely képes felismerni, mely faj(ok) hallhatók az adott hangmintában.

## Repo felépítése

### Könyvtárstruktúra
```bash
.
├── data/
│   ├── train_audio/
│   │   ├── asbfly/
│   │   ├── ashdro1
│   │   ├── .../
│   ├── train_metadata.csv
├── data_visualisation.ipynb

```

## Tanítás

A tanítás indításához a *training_and_evaluation.ipynb* fájl celláinak futtatására van szükség. A kiértékelés az utolsó cellában történik, ahol az adathalmaz egy elkülönített szegmensén ellenőrizzük a legjobban teljesítő modell pontosságát.

### Adatok betöltése

A tanító adathalmaz egy nyilvánosan megosztott Drive mappában található, innen történik meg a betöltés. A futtatáskor nincs szükség semmilyen autentikációra.

### A háló architektúrája

Az általunk használt neurális háló az [EfficientNetV2](https://arxiv.org/abs/2104.00298) architektúrára épül. Ez a korábbi CNN modellekhez képest gyorsabb tanítási időt és jobb paraméterhatékonyságot biztosít.