# Projekodumu
ödev
import random

secenek = ["taş", "kağıt", "makas"]
taş = secenek[0]
kağıt = secenek[1]
makas = secenek[2]
senin_skorun = 0
bilg_skor = 0
print(
    "Taş,kağıt,makas oyununa hoş geldiniz. Oyundan çıkmak için q tuşuna basınız.\n5 skoruna ulaşan kazanır, bol şans!!!\n")

while True:
    bilg_secim = random.choice(secenek)
    secim = input("Sezgilerine güven. Taş mı kağıt mı makas mı? ")

    if secim == taş:
        if bilg_secim == taş:
            print("Bilgisayar taş seçti, sonuç: Berabere\n")
        elif bilg_secim == makas:
            senin_skorun = senin_skorun + 1
            if senin_skorun == 5:
                print("Senin puanın: {} , Bilgisayarın puanı: {}\n".format(senin_skorun, bilg_skor))
                print("Oyun bitti. Kazandınız!!!")
                break
            else:
                print("Bilgisayar makas seçti, sonuç: Kazandınız")
                print("Senin puanın: {} , Bilgisayarın puanı: {}\n".format(senin_skorun, bilg_skor))

        else:
            bilg_skor = bilg_skor + 1
            if bilg_skor == 5:
                print("Senin puanın: {} , Bilgisayarın puanı: {}\n".format(senin_skorun, bilg_skor))
                print("Oyun bitti. Kaybettiniz...")
                break
            else:
                print("Bilgisayar kağıt seçti, sonuç: Kaybettiniz")
                print("Senin puanın: {} , Bilgisayarın puanı: {}\n".format(senin_skorun, bilg_skor))

    elif secim == kağıt:
        if bilg_secim == kağıt:
            print("Bilgisayar kağıt seçti, sonuç: Berabere\n")
        elif bilg_secim == taş:
            senin_skorun = senin_skorun + 1
            if senin_skorun == 5:
                print("Senin puanın: {} , Bilgisayarın puanı: {}\n".format(senin_skorun, bilg_skor))
                print("Oyun bitti. Kazandınız!!!")
                break
            else:
                print("Bilgisayar taş seçti, sonuç: Kazandınız")
                print("Senin puanın: {} , Bilgisayarın puanı: {}\n".format(senin_skorun, bilg_skor))

        else:
            bilg_skor = bilg_skor + 1
            if bilg_skor == 5:
                print("Senin puanın: {} , Bilgisayarın puanı: {}\n".format(senin_skorun, bilg_skor))
                print("Oyun bitti. Kaybettiniz...")
                break
            else:
                print("Bilgisayar makas seçti, sonuç: Kaybettiniz")
                print("Senin puanın: {} , Bilgisayarın puanı: {}\n".format(senin_skorun, bilg_skor))

    elif secim == makas:
        if bilg_secim == makas:
            print("Bilgisayar makas seçti, sonuç: Berabere\n")
        elif bilg_secim == kağıt:
            senin_skorun = senin_skorun + 1
            if senin_skorun == 5:
                print("Senin puanın: {} , Bilgisayarın puanı: {}\n".format(senin_skorun, bilg_skor))
                print("Oyun bitti. Kazandınız!!!")
                break
            else:
                print("Bilgisayar kağıt seçti, sonuç: Kazandınız")
                print("Senin puanın: {} , Bilgisayarın puanı: {}\n".format(senin_skorun, bilg_skor))
        else:
            bilg_skor = bilg_skor + 1
            if bilg_skor == 5:
                print("Senin puanın: {} , Bilgisayarın puanı: {}\n".format(senin_skorun, bilg_skor))
                print("Oyun bitti. Kaybettiniz...")
                break
            else:
                print("Bilgisayar taş seçti, sonuç: Kaybettiniz")
                print("Senin puanın: {} , Bilgisayarın puanı: {}\n".format(senin_skorun, bilg_skor))

    else:
        if secim == "q":
            print("Çıkılıyor...")
            break
