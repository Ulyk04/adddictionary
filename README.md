# adddictionary
This function is unite two different dictionary
def add(d1, d2):
    yeni_sozluk = d1.copy()

    for anahtar, deger in d2.items():
        if anahtar in yeni_sozluk:
            yeni_sozluk[anahtar][0] += deger[0]  # İlk elemanları topla
            yeni_sozluk[anahtar][1] += deger[1]  # İkinci elemanları topla
        else:
            yeni_sozluk[anahtar] = deger

    return yeni_sozluk


d1 = {"GS": [8, 1], "FB": [6, 3]}
d2 = {"GS": [2, 0], "BJK": [5, 4]}

yeni_d1 = add(d1, d2)
print(yeni_d1)
