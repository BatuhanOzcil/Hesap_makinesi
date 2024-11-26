You can see the code below:

    def main():
        while True:
            try:
                first_number=int(input("Lütfen ilk sayıyı giriniz: "))
                second_number=int(input("Lütfen ikinci sayıyı giriniz: "))
            except ValueError:
                    print("Lütfen tam sayi giriniz.")
                    continue
    
            operator=input("Lütfen işlemi seçin [+,-,*,/] (Çıkmak için 'ç' ye basın) ->")
            if operator == "ç":
                print("Program sonlandırıldı.")
                break
            elif operator == "+" :
                toplama=first_number+second_number
                print(f"Sonuç: {toplama}")
            elif operator=="-":
                çıkarma=first_number-second_number
                print(f"Sonuç: {çıkarma}")
            elif operator=="*":
                çarpma=first_number*second_number
                print(f"Sonuç: {çarpma}")
            elif operator=="/":
                if second_number==0:
                    print("Bir sayıyı 0'a bölemezsiniz.")
                else:
                    bölme=first_number/second_number
                    print(f"Sonuç: {bölme}")
            else:
                print("Geçersiz bir işlem girdiniz.")
        return
    main()
