# Pity Func

Disini Kamu Akan Mempelajari Sistem **Pity** Di bot Kisaki.

## Apa Itu Pity?

**Pity** adalah sistem yang digunakan dalam gacha untuk meningkatkan Chance mendapatkan Waifu setelah melakukan beberapa kali `!wgacha` tanpa mendapatkan Waifu yang diinginkan. Setiap kali gagal, Chance untuk mendapatkan waifu yang lebih baik akan meningkat, tergantung pada jumlah pity yang telah terkumpul.

## Perhitungan Pity dan Chance

| Pity Range    | Multiplier Pity | Chance (Tingkat Kesulitan)                                                                 | Chance Maksimal   | Rcrystal dan Karisma Level       |
|---------------|-----------------|---------------------------------------------------------------------------------------------|--------------------|----------------------------------|
| **0 - 49**    | 1.0             | - Mudah: 45%<br>- Sedang: 25%<br>- Sulit: 10%<br>- Mustahil: 2%                              | 95% (Mudah)        | **Mudah**: 20-39 Rcrystal<br>50-99 Karisma  |
| **50 - 84**   | 1.0 + (Pity * 0.008) | - Mudah: 45%<br>- Sedang: 25%<br>- Sulit: 10%<br>- Mustahil: 2%                              | 85% (Sedang)       | **Sedang**: 40-89 Rcrystal<br>100-249 Karisma |
| **85 - 129**  | 1.4 + ((Pity - 50) * 0.012) | - Mudah: 45%<br>- Sedang: 25%<br>- Sulit: 10%<br>- Mustahil: 2%                              | 75% (Sulit)        | **Sulit**: 90-139 Rcrystal<br>250-999 Karisma |
| **130 - 179** | 1.82 + ((Pity - 85) * 0.016) | - Mudah: 45%<br>- Sedang: 25%<br>- Sulit: 10%<br>- Mustahil: 2%                              | 65% (Mustahil)     | **Mustahil**: 140-200+ Rcrystal<br>1000+ Karisma |
| **180+**      | 3.5             | - Mudah: 45%<br>- Sedang: 25%<br>- Sulit: 10%<br>- Mustahil: 2%                              | 65% (Mustahil)     | **Mustahil**: 140-200+ Rcrystal<br>1000+ Karisma |

### Penjelasan:
- **Pity Range**: Rentang pity berdasarkan jumlah `!wgacha` yang telah dilakukan.
- **Multiplier Pity**: Nilai yang digunakan untuk meningkatkan Chance berdasarkan jumlah pity.
- **Chance (Tingkat Kesulitan)**: Chance mendapatkan waifu berdasarkan tingkat kesulitan yang ditetapkan dalam sistem. Nilai Chance ini dapat meningkat seiring dengan bertambahnya pity.
- **Chance Maksimal**: Batasan Chance maksimal yang dapat dicapai untuk setiap tingkat kesulitan.
- **Rcrystal dan Karisma Level**: Rcrystal Di Gunakan Saat Km Melakukan `!wdivorce` Dan Mendapat Kan Rcrystal Karena Ktu, **Karisma** Adalah Power Wakfu Semakin Tinggi semakin populer.


> **⚠️ Disclaimers:** 
Pity Akan Di reset kembali setelah kamu mendapatkan waifu karena pity misal pity kamu 80+ dan kamu mendapatkan waifu dengan kesulitan sedang karena buff pity tsb, maka pity kamu akan **di reset**


## Sistem Pilih Waifu

Sistem **Pilih Waifu** di bot Kisaki menggunakan logika berikut:
1. **Tingkat Kesulitan** dipilih berdasarkan nilai pity.
2. **Chance** waifu di hitung dari tingkat kesulitan waifu dan juga pity.
3. **Variasi Chance** dapat dipengaruhi oleh pity, dengan kemungkinan waifu memiliki Chance lebih tinggi tergantung pada pity yang terkumpul.

### Tabel Tingkat Kesulitan Berdasarkan Pity:

| Pity Range   | Tingkat Kesulitan yang Tersedia  |
|--------------|-----------------------------------|
| 0 - 49       | Mudah, Sedang                    |
| 50 - 84      | Mudah, Sedang, Sulit, Mustahil   |
| 85 - 129     | Mudah, Sedang, Sulit, Mustahil   |
| 130 - 179    | Mudah, Sedang, Sulit, Mustahil   |
| 180+         | Sulit, Mustahil                  |

## Contoh Perhitungan

Misalnya, jika pemain memiliki **pity 100**, maka sistem akan menghitung Chance mereka untuk mendapatkan waifu dengan tingkat kesulitan yang lebih tinggi, seperti **Sulit** atau **Mustahil**, dengan Chance yang lebih besar dari `!wgacha` yang sebelumnya.

### Update Rcrystal dan Karisma

Selain Chance gacha, setiap waifu memiliki nilai **Rcrystal** dan **Karisma_level** yang ditentukan berdasarkan tingkat kesulitannya:

| Tingkat Kesulitan | Rcrystal         | Karisma Level     |
|-------------------|-----------------|--------------------|
| **Mudah**         | 20-39 Rcrystal   | 50-99 Karisma     |
| **Sedang**        | 40-89 Rcrystal   | 100-249 Karisma   |
| **Sulit**         | 90-139 Rcrystal  | 250-999 Karisma   |
| **Mustahil**      | 140-200+ Rcrystal| 1000+ Karisma     |

Dengan memahami sistem **Pity**, **Rcrystal**, dan **Karisma** ini, kamu bisa lebih merencanakan langkah-langkahmu dalam memperoleh waifu yang diinginkan!

---