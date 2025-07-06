# **Komronbek Atavullayev \- Turizm Menejeri Portfoliosi**

Bu Komronbek Atavullayevning turizm menejeri sifatidagi shaxsiy portfoliosi bo'lib, uning ko'nikmalari, tajribasi, ta'limi va loyihalarini namoyish etadi. Veb-sayt mijozlarga yuqori sifatli xizmat ko'rsatishga va unutilmas sayohat tajribalarini yaratishga intiluvchi yosh va g'ayratli mutaxassisni taqdim etadi.

## **Xususiyatlari**

* **Interaktiv va Dinamik Dizayn:** Tailwind CSS yordamida to'liq responsiv va zamonaviy UI.  
* **Ko'p tillilik:** O'zbek, Rus, Ingliz va Turk tillarini qo'llab-quvvatlaydi.  
* **Dark Mode (Qorong'u rejim):** Foydalanuvchilar uchun qulay ko'rish tajribasi.  
* **Real-time Clock (Haqiqiy vaqt soati):** Joriy vaqtni ko'rsatadi.  
* **Ko'nikmalar bo'limi:** Tillar bilimi va kompyuter savodxonligi bo'yicha ma'lumotlar.  
* **Ish tajribasi va ta'lim:** Vaqt jadvali (timeline) shaklida taqdim etilgan.  
* **Loyihalar bo'limi:** Ishlab chiqilgan loyihalarni namoyish etish uchun.  
* **Aloqa formasi:** Xabarlarni yuborish imkoniyati.  
* **Google AdSense integratsiyasi:** Reklama ko'rsatish imkoniyati.  
* **404 Sahifa:** Topilmagan sahifalar uchun maxsus dizayn.  
* **Yuqoriga/Pastga aylantirish tugmasi:** Sahifada navigatsiya qilishni osonlashtiradi.  
* **Preloader:** Sahifa yuklanayotganda animatsion preloader.

## **Texnologiyalar**

* **HTML5:** Veb-sahifa tuzilishi uchun.  
* **CSS3:** Veb-sahifa uslublari uchun.  
* **Tailwind CSS:** Tez va responsiv dizayn uchun.  
* **JavaScript (ES6+):** Interaktivlik va dinamik xususiyatlar uchun.  
* **Font Awesome:** Ikonkalar uchun.  
* **jQuery:** (Ixtiyoriy, ammo mavjud) DOM manipulyatsiyasi uchun.  
* **Firebase:**  
  * **Firebase Hosting:** Saytni joylashtirish uchun.  
  * **Firebase Authentication:** Foydalanuvchi autentifikatsiyasi.  
  * **Firebase Firestore:** Aloqa formasidan yuborilgan xabarlarni saqlash uchun.  
* **Google AdSense:** Reklama ko'rsatish uchun.

## **O'rnatish va Sozlash**

Loyihani mahalliy kompyuteringizda ishga tushirish yoki Firebase'ga joylashtirish uchun quyidagi qadamlarni bajaring:

### **1\. Loyihani yuklab olish**

Agar sizda Git o'rnatilgan bo'lsa, loyihani klonlashingiz mumkin (agar u Git repozitoriyasida bo'lsa):

git clone \<sizning-repo-manzilingiz\>  
cd \<loyihangiz-papkasi\>

Yoki shunchaki index.html faylini va unga tegishli barcha resurslarni (CSS, JS, rasmlar) bir papkaga yuklab oling.

### **2\. Firebase CLI'ni o'rnatish**

Agar sizda hali o'rnatilmagan bo'lsa, Node.js va npm (Node Package Manager) o'rnatilganligiga ishonch hosil qiling. Keyin Firebase buyruq qatori interfeysini (CLI) global ravishda o'rnating:

npm install \-g firebase-tools

### **3\. Firebase'ga kirish**

Terminalda Firebase hisobingizga kiring:

firebase login

Bu sizni brauzerga yo'naltiradi va Google hisobingizga kirishni so'raydi.

### **4\. Firebase loyihasini initsializatsiya qilish**

Loyihangiz papkasida (ya'ni, index.html fayli joylashgan joyda) quyidagi buyruqni ishga tushiring:

firebase init

Savollarga quyidagicha javob bering:

* **"Which Firebase features do you want to set up for this directory?"**: Hosting ni tanlang.  
* **"Please select a project:"**: Mavjud Firebase loyihangizni tanlang yoki yangisini yarating.  
* **"What do you want to use as your public directory?"**: Agar index.html faylingiz papkaning o'zida bo'lsa, **.** (nuqta) deb yozing. Aks holda, saytingiz fayllari joylashgan papka nomini kiriting (masalan, public).  
* **"Configure as a single-page app (rewrite all urls to /index.html)?"**: **"No"** deb tanlang.  
* **"Set up automatic builds and deploys with GitHub?"**: Bu ixtiyoriy.

### **5\. Google AdSense'ni sozlash**

1. **AdSense hisobiga kirish:** [adsense.google.com](https://adsense.google.com/) manziliga o'ting va hisobingizga kiring.  
2. **Reklama bloki yaratish:** AdSense hisobingizda reklama bloki yarating va data-ad-slot ID'sini oling.  
3. **Kodni yangilash:** index.html faylingizdagi reklama blokida YOUR\_AD\_SLOT\_ID\_HERE joyini o'zingizning haqiqiy data-ad-slot ID'ingiz bilan almashtiring.  
   \<ins class="adsbygoogle"  
        style="display:block; text-align:center;"  
        data-ad-layout="in-article"  
        data-ad-format="fluid"  
        data-ad-client="ca-pub-2435346542328852"  
        data-ad-slot="YOUR\_AD\_SLOT\_ID\_HERE"\>\</ins\>

4. **AdSense tasdiqlashini kutish:** Reklamalar saytingizda ko'rinishi uchun AdSense saytingizni to'liq tasdiqlashi kerak.

### **6\. Firebase'ga joylashtirish**

Barcha sozlashlar tugagandan so'ng, loyihangizni Firebase Hosting'ga joylashtirish uchun quyidagi buyruqni ishga tushiring:

firebase deploy

Bu buyruq loyihangizni internetga joylashtiradi va sizga saytingizning URL manzilini beradi.

## **Foydalanish**

Veb-saytni ishga tushirgandan so'ng:

* **Tilni almashtirish:** Yuqori o'ng burchakdagi "Tilni almashtirish" tugmasini bosing yoki mobil menyudan tilni tanlang.  
* **Dark Mode:** Yuqori o'ng burchakdagi tugma orqali qorong'u rejimni yoqing/o'chiring.  
* **Aloqa formasi:** "Aloqa" bo'limidagi formani to'ldirib, Komronbekka xabar yuboring.  
* **Ko'nikmalar/Shaxsiy fazilatlar:** Tegishli bo'lim sarlavhalarini bosib, ma'lumotlarni kengaytiring yoki yig'ing.

## **Aloqa**

Agar savollaringiz bo'lsa yoki hamkorlik qilishni istasangiz, Komronbek Atavullayev bilan quyidagi ma'lumotlar orqali bog'lanishingiz mumkin:

* **Elektron pochta:** kamronatavullayev@gmail.com  
* **Telefon:** \+998 91 954 93 24, \+998 88 822 33 25  
* **Manzil:** Qashqadaryo viloyati, Qarshi shahri, Tabassum mahallasi  
* **Ijtimoiy tarmoqlar:**  
  * [Instagram](https://www.google.com/search?q=https://www.instagram.com/1.kamronbek.1)  
  * [WhatsApp](https://www.google.com/search?q=https://wa.me/998330101245)  
  * [Facebook](https://www.google.com/search?q=https://www.facebook.com/kamronatavullayev3)  
  * [YouTube](https://www.youtube.com/c/ZipNationSongs)  
  * [Telegram](https://www.google.com/search?q=https://t.me/Kamronlife)

## **Litsenziya**

Ushbu loyiha aniq ochiq manbali litsenziya ostida emas. Barcha huquqlar mualliflik huquqi bilan himoyalangan. Loyihaning mazmuni va dizaynidan foydalanish yoki uni o'zgartirishdan oldin muallif bilan bog'lanish tavsiya etiladi.