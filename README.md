# Kelajak soatları — BMAR viktorinası (Firebase + Vercel)

Bul nusqa 12 sorawlı viktorina hám barlıq qurılmalarda birdey, real waqıtta jańalanatuǵın reyting ushın tayarlanǵan.

## Fayllar
- `index.html` — sayt
- `README.md` — sazlaw boyınsha qollanba

## 1. Firebase Realtime Database jaratıw
1. https://console.firebase.google.com/ betine kiriń hám jańa project jaratıń.
2. Project ishinde **Build → Realtime Database → Create Database** bólimine ótiń.
3. Database location tańlań. Seminar ushın jańa, bólek database paydalanıń.
4. **Project settings → General → Your apps** bóliminde Web app (`</>`) qosıń. App config mánislerin kóshirip alıń.
5. Firebase konfiguraciyası `index.html` ishine qosılǵan. Deploy etiwden aldın Firebase Console-dan database URL durıs ekenin tekseriń.

## 2. Database rules
Test ushın Firebase Console → Realtime Database → **Rules** bóliminde tómendegi qáǵıydalardı ornatıw múmkin:

```json
{
  "rules": {
    "kelajakBMAR": {
      ".read": true,
      ".write": true
    }
  }
}
```

**Qáwipsizlik eskertpesi:** bul ashıq qáǵıydalar bolǵanı ushın, linkti bilgen hár kim nátiyjelerdi oqıwı, qosıwı yamasa ózgertiwi múmkin. Bul tek qısqa seminar/demo ushın. Jeke maǵlıwmat jazbań. Seminar tamamlanǵannan keyin Rules arqalı jazıwdı jawıń yamasa autentifikaciya hám server tárepindegi tekseriw qosıń. Bul HTML faylındaǵı ball esaplaw brauzerde boladı, sonlıqtan texnikalıq jaqtan ózgertiw múmkin.

## 3. GitHubqa júklew
1. https://github.com/new betinde `kelajak-soatlari-bmar` degen repository jaratıń.
2. `index.html` hám `README.md` faylların repository-ǵa júkleń.
3. `index.html` repository-ńizdiń root bóliminde bolıwı kerek.

## 4. Vercelge deploy etiw
1. https://vercel.com/new betine kiriń.
2. GitHub repository-ńizdi import etiń.
3. Bul ápiwayı statikalıq sayt: build command hám framework preset talap etilmeydi (Other/None tańlawǵa boladı).
4. **Deploy** basıń. Vercel bergen `*.vercel.app` linkin qatnasıwshılarǵa jiberiń.

## 5. Test
- Sayttı ashıp, bir test atı menen 2-3 sorawǵa juwap berip, nátiyjeni ayaqlap saqlap kóriń.
- Ekinshi telefon/Incognito brauzerde sayttı ashıp, basqa at penen nátiyje qosıń.
- Eki qurılmada da reyting jańalanǵanın tekseriń.

## Eskertiw
Bul demo bir at penen qayta qatnasıwǵa sheklew qoymaydı. Firebase config web bette kórinedi — bul Firebase web app-lar ushın ádettegi jaǵday; qáwipsizlikti database rules hám autentifikaciya menen basqarıw kerek.
