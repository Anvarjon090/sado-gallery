# Sado Gallery

Sado ilovasi uchun standart ovozlar to'plami. `manifest.json` ni Sado o'zi o'qiydi;
ovozlar faqat foydalanuvchi "Yuklab olish" degandan keyin yuklanadi.

## Sado standart ovozlari

| Ism | Ovoz | Vazifasi |
|---|---|---|
| Nilufar | female, middle-aged, moderate pitch | Aniq va ishonchli diktor ovozi — yangiliklar, e'lonlar, o'quv materiallari. |
| Madina | female, middle-aged, low pitch | Yumshoq, past ohangli hikoyachi — audiokitob va uzun matnlar. |
| Sevara | female, young adult, moderate pitch | Yosh, iliq ovoz — ertaklar, bolalar kontenti, do'stona suhbat. |
| Jahongir | male, middle-aged, low pitch | Salobatli diktor ovozi — yangiliklar, hujjatli filmlar, rasmiy matnlar. |
| Bobur | male, young adult, moderate pitch | Quvnoq, g'ayratli ovoz — reklama, ijtimoiy tarmoq videolari, suhbat. |
| Qodir | male, elderly, low pitch | Keksa, bosiq hikoyachi — ertak, xotiralar, hikmatli matnlar. |

Hamma ovozlar **sintetik**: OmniVoice ovoz dizayni orqali matnli tavsifdan
yaratilgan, hech kimning real ovozidan klonlanmagan. Har bir ovoz o'zbek, rus va
ingliz tillarida sinalgan (o'zbekcha tushunarlilik: CER < 2.5%, uzstt bilan o'lchangan).

## Sxema

Upstream VoiceStudio galereyasi bilan bir xil (`type: "voice"` elementlar, `packs`).
`audio.sha256` yuklab olingan faylni tekshirish uchun ishlatiladi; faylni
o'zgartirsangiz, hash'ni ham yangilang.

## Litsenziya

Audio namunalar: OpenRAIL-M (OmniVoice modeli chiqishiga mos). Matn va manifest: CC0.
