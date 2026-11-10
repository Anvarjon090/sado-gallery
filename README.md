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

## Sxema

Upstream VoiceStudio galereyasi bilan bir xil: `items` (`type: "voice"`,
`audio.url` GitHub'da, `audio.sha256`, `audio.ref_text`) va `packs`.
`sado-starter` to'plami haqiqiy ovozlar qo'shilganda qaytadi.

## Litsenziya

Matn va manifest: CC0. Har bir ovozning litsenziyasi o'z `license` maydonida.
