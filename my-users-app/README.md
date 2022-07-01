
# my-users-app
User creat (foydalanuvchi yaratish)
curl -X POST -i http://localhost:8080/users -d "firstname=umarxoja" -d "lastname=xikmatxojaev" -d "age=25" -d "password=88888888" -d "email=umar0528@gmail.com"

Than open (keyin shu vebsaytni oching)
https://web-wdf97c006-5f08.docodev2.qwasar.io/

Sign in (ro'yxatdan o'tish)
curl -c cookies.txt -X POST localhost:8080/sign_in -d email=umar0528@gmail.com -d password=88888888

update (parolni yangilash): (bu ishlashi uchun avval sign_in qilish kerak) (you need to sign_in first for this to work)
curl -b cookies.txt -X PUT localhost:8080/users -d password=ikkinchikod

sign out (akkountdan chiqish): (bu ishlashi uchun avval sign_in qilish kerak) (you need to sign_in first for this to work)
curl -b cookies.txt -X DELETE localhost:8080/sign_out 

delete (akkountni butunlay o'chirib tashlash): (bu ishlashi uchun avval sign_in qilish kerak) (you need to sign_in first for this to work)
curl -b cookies.txt -X DELETE localhost:8080/users
