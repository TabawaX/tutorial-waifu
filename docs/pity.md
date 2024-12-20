## Penjelasan Fungsi `pity`

| **Bagian**                      | **Deskripsi**                                                                                                                                             |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Base Chances**                 | chance dasar untuk setiap base difficulty:                                                                                                            |
|                                  | - **easy**: 0.85 (85%)                                                                                                                                  |
|                                  | - **medium**: 0.10 (10%)                                                                                                                                 |
|                                  | - **hard**: 0.04 (4%)                                                                                                                                   |
|                                  | - **impossible**: 0.01 (1%)                                                                                                                                |
| **Penyesuaian Berdasarkan Pity** | chance ditingkatkan berdasarkan nilai `pity`:                                                                                                          |
| **Pity 50 - 99**                 | - **medium** + 5%                                                                                                                                         |
|                                  | - **hard** + 1%                                                                                                                                         |
| **Pity 100 - 199**               | - **medium** + 10%                                                                                                                                       |
|                                  | - **hard** + 3%                                                                                                                                         |
|                                  | - **impossible** + 1%                                                                                                                                      |
| **Pity 200+**                    | - **medium** + 15%                                                                                                                                       |
|                                  | - **hard** + 5%                                                                                                                                        |
|                                  | - **impossible** + 2%                                                                                                                                      |
| **Pity Minimum untuk Hard dan Impossible** | Jika `pity` kurang dari 100, maka chance untuk memilih waifu **hard** dan **impossible** adalah 0%                                                    |
| **Pity Bonus**                   | Setiap nilai `pity` ditambahkan bonus chance yang dihitung dengan rumus: `pity * 0.0001`                                                              |
| **Probabilitas Normalisasi**     | chance yang sudah disesuaikan dengan pity akan dinormalisasi agar total probabilitasnya menjadi 1.                                                      |
| **CDF (Cumulative Distribution Function)** | Membuat distribusi kumulatif berdasarkan probabilitas yang sudah dinormalisasi untuk memudahkan pemilihan base difficulty secara acak                 |
| **Pemilihan Waifu**              | Setelah base difficulty terpilih, waifu dipilih secara acak berdasarkan base difficulty yang telah ditentukan. Jika tidak ada waifu dengan difficulty tersebut, maka waifu acak dipilih. |