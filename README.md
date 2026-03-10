import random

characters = "+-/*!&$#?=@abcdefghijklnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ1234567890"

def generate_password(Length: int):

    password = ""

    for i in range(length):

        password += random.choice(characters)

    return password
def save_passwords(account: str, password: str):
    with open("passwords.txt", "a", encoding="utf8")as file:  
        file.write(f"{account} hesabı şifren: {password}\n")

account_name=input("Hangi Hesabın Için Şifre Istiyorsun?\n")
length = int(input("Şifren Kaç Karakterli Olsun?\n"))
password = generate_password(length)
save_passwords(account_name,password)
print(password)

belki ihtiyacınız olur :P
