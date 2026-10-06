# Housing Services (vyuo vyote vya Dar es Salaam): jinsi ya kuweka (dakika 15)

Mradi una kurasa tatu:

- `index.html`: wateja wanaona vyumba vilivyokubaliwa, wanachuja kwa chuo, aina na bei, kisha wanapiga simu au WhatsApp. Kabla ya kuunganisha Firebase inaonyesha vyumba vya mfano.
- `dalali.html`: madalali wanajisajili, wanaweka chumba (chuo kilicho karibu, picha 1 hadi 3, maelezo, bei, eneo, simu) na wanasimamia vyumba vyao.
- `admin.html`: wewe unakubali au unakataa kila chumba kabla hakijaonekana. Usiweke link yake popote kwa wateja.

## Hatua

1. Nenda https://console.firebase.google.com, bonyeza **Add project**, ipe jina (mfano `housing-services-ifm`).
2. **Build > Authentication > Get started**, washa **Email/Password**.
3. **Build > Firestore Database > Create database**, chagua **Production mode** na eneo lililo karibu.
4. **Project settings (gia) > Your apps > Web (`</>`)**, sajili app, kisha nakili `firebaseConfig`. Fungua `lib.js` na ubadilishe thamani za `PASTE_...`.
5. Kwenye Firestore, fungua tab ya **Rules**, futa vilivyopo, bandika yaliyomo kwenye `firestore.rules`, bonyeza **Publish**.
6. Weka wewe kama admin:
   - Fungua `dalali.html` kisha **Jisajili** kwa barua pepe yako.
   - Kwenye Firebase **Authentication > Users**, nakili **User UID** yako.
   - Kwenye Firestore, **Start collection** jina `admins`, **Document ID** = UID uliyonakili, weka field yoyote (mfano `role` = `admin`), hifadhi.
   - Sasa unaweza kuingia kwenye `admin.html`.
7. Weka mtandaoni (bure): **Firebase Hosting**, Netlify (buruta folda), au GitHub Pages. Kisha kwenye **Authentication > Settings > Authorized domains** ongeza domain ya website yako.

## Jinsi inavyofanya kazi

- Dalali akituma chumba, hali yake ni `pending`. Wateja hawakioni mpaka ukikubali kwenye `admin.html`.
- Dalali anaweza kuweka chumba kuwa "imechukuliwa" au kukifuta. Hawezi kubadilisha hali ya kukubaliwa.
- Picha zinapunguzwa ukubwa na kuhifadhiwa ndani ya Firestore, kwa hiyo huhitaji Firebase Storage. Orodha hupakia picha ndogo tu, picha kubwa zinapakiwa mteja akifungua chumba.

## Mipaka ya version one

- Dalali hawezi kuhariri chumba, afute na aweke upya.
- Vyuo vimeandikwa kwenye `lib.js` (`CHUO`) na kwenye `index.html`. Ukitaka kuongeza chuo, ongeza mahali hapo mbili.
- Hakuna uthibitisho wa barua pepe, ukaguzi wako wa admin ndio kinga ya matangazo ya uongo.
- Firebase ina kikomo cha bure cha kusoma data kwa siku. Ukikua sana, ongeza mpango.

## Kujaribu kabla ya kuwaambia madalali

1. Fungua `index.html`. Ukiona vyumba vya mfano, config bado haijawekwa. Ukiona "Vyumba havikupatikana", angalia rules na domain.
2. Jisajili kwenye `dalali.html`, tuma chumba chenye picha.
3. Ingia `admin.html`, kikubali.
4. Fungua `index.html`, chuja kwa chuo ulichochagua, fungua chumba na ujaribu WhatsApp.
