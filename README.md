# Sado Gallery

Sado ilovasi uchun standart ovozlar to'plami. `manifest.json` ni Sado o'zi o'qiydi;
ovozlar faqat foydalanuvchi "Yuklab olish" degandan keyin yuklanadi.

## Holat

To'plam hozircha **bo'sh**. 2026-11-10 da sintetik (ovoz dizayni bilan yaratilgan)
oltita ovoz olib tashlandi: reference sifatida faqat haqiqiy inson yozuvi
ishlatiladi, TTS/AI audio emas — natija sun'iy bo'lib qoladi.

## Ovoz qabul qilish qoidalari

1. Faqat haqiqiy inson yozuvi, roziligi bilan (o'z ovozi, rozi odam, Common Voice
   CC0 yoki ochiq litsenziyali yozuv — litsenziya yozib qo'yiladi).
2. 12–20 soniya, bitta uzluksiz gap; musiqa, shovqin, reverb, telefon effekti
   yoki ikkinchi ovoz yo'q.
3. Bitta odam, tabiiy ohang: neytral yoki iliq, shoshilmasdan.
4. Mono WAV, 24 kHz yoki yuqori, 16-bit; peak −3 dBFS. Fayl: `<ism>_<til>_<jins>.wav`.
5. Ref matn — audio aynan nima deyilgani, so'zma-so'z, ASCII apostrof (').
6. Metama'lumot: ism, til, jins, yosh, sheva/mintaqa, ref matn, manba, litsenziya.
7. Qabuldan oldin shu ovoz bilan bitta gap generatsiya qilinib eshitiladi.

Tekshiruv vositasi Sado repo'sida: `scripts/voice_intake.py` — o'lchaydi,
masterlaydi, metama'lumot yozadi va sinov gapini generatsiya qiladi.
Model (OmniVoice) o'zi 3–10 soniyalik namunani tavsiya qiladi va 20 s dan
uzunini ogohlantiradi; 15 s dan uzun yozuvda eng toza 8–12 soniyalik bo'lak
kesib olinadi.

## Olti ovoz — kasting varaqasi

Ovoz shaxsiyati faqat haqiqiy yozuvdan keladi: model tembr, nafas, ohang va
yozuv muhitini namunadan ko'chiradi. "Ovoz dizayni" rejimi esa faqat jins,
yosh va baland-pastlikni biladi — u bilan olti xil shaxs chiqmaydi, faqat olti
xil balandlik chiqadi. Shuning uchun har bir rol uchun alohida odam yoziladi.

| Rol | Yosh taassuroti | Tembr / ohang | F0 (taxminan) | Matn turi (yozuv uchun) |
|---|---|---|---|---|
| Tabiiy yosh ayol | 20–27 | iliq, aniq, do'stona suhbat; sun'iy shirinlik yo'q | 190–250 Hz | kundalik suhbat, 2–3 gap |
| Professional ayol diktor | 28–40 | ishonchli, to'la rezonans, aniq artikulyatsiya | 165–220 Hz | yangilik yoki e'lon matni |
| Ayol hikoyachi | 30–45 | iliq, ifodali, intensivlik o'zgarib turadi | 160–230 Hz | ertak yoki hikoya parchasi |
| Tabiiy yosh erkak | 20–30 | bo'shashgan, o'rta-past, kundalik ohang | 100–140 Hz | kundalik suhbat |
| Professional erkak diktor | 30–45 | chuqur, lekin tabiiy; kuchli rezonans | 85–125 Hz | yangilik yoki e'lon matni |
| Keksa erkak | 65–80 | yoshga xos yengil xirillash, shoshilmas sur'at | 95–150 Hz | xotira, nasihat ohangidagi hikoya |

Yozuv talablari hamma rol uchun bir xil (yuqoridagi qoidalar). Rol uchun
matnni o'sha rolning ohangida o'qish kerak: diktor matnini hikoyachi ohangida
o'qigan yozuv diktorga yaramaydi — model ohangni ham ko'chiradi.

Namunani `scripts/voice_intake.py ... --install --check` bilan tekshirib,
sinov gapini eshitib, keyin shu repo'ga `voices/<ism>_<til>_<jins>.wav` va
`manifest.json` yozuvi sifatida qo'shiladi.

## Sxema

Upstream VoiceStudio galereyasi bilan bir xil: `items` (`type: "voice"`,
`audio.url` GitHub'da, `audio.sha256`, `audio.ref_text`) va `packs`.
`sado-starter` to'plami haqiqiy ovozlar qo'shilganda qaytadi.

## Litsenziya

Matn va manifest: CC0. Har bir ovozning litsenziyasi o'z `license` maydonida.
