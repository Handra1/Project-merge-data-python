# Project-merge-data-python
This project about learning merge data in python (In Indonesia)

Concatenating data dapat dianggap sebagai menyatukan data yang dulunya merupakan dataset tunggal. Tetapi itu bukan satu-satunya cara data dapat digabungkan. Cara lainnya adalah dengan melakukan merge data.
Merging Data:
1. Mirip dengan perintah join table di SQL.
2. Menggabungkan dataset yang berbeda berdasarkan kolom umum

Terdapat 3 Tipe Merging Data:
1. One-to-one
2. Many-to-one/ One-to-many
3. Many-to-many

Merging Data One-to-one:
Kita dapat mengkombinasikan 2 dataset diatas dengan cara mencocokan kolom state. Disini kolom kunci yang kita pakai adalah “state” yang ada di sebelah kiri dataframe dan kolom “name” yang ada di sebelah kanan dataframe. Sehingga ketika kita melakukan proses merge untuk kolom yang telah sesuai dicocokan, langkah selanjutnya adalah membuatnya menjadi dataframe baru. Untuk melakukan proses join kita gunakan fungsi merge di dalam Pandas. Karena nama kolom unik dari masing - masing datasets memiliki nama yang berbeda, maka kita harus menuliskan parameter left_on dan right_on. Hasil dari proses merge ini, sekarang kita memiliki semua kolom state, population dan singkatan dalam 1 dataset. Contoh kasus ini juga termasuk dalam one-to-one merging data, karena dataframes sebelah kiri dan dataframe sebelah kanan semuanya memiliki kunci yang sesuai 1-to-1.

Merging Data Many-to-one/One-to-many:
Jika terdapat nilai duplikat di salah satu kunci, maka nilai dari kunci lain akan terulang kembali yang mengakibatkan menjadi duplikat. Pada gambar diatas terdapat banyak nama kota untuk masing - masing negara bagian (state). Ketika kita mengkombinasikan dataset city dengan dataset kode state maka hasilnya akan seperti ini:
Nilai dari dataset kode state akan menjadi duplikat untuk masing - masing city. Ini merupakan contoh one-to-many atau many-to-one merging data. Kesimpulannya adalah untuk mengatasi 3 tipe merging data tersebut, semuanya kita bisa gunakan fungsi yang sama yaitu: merge.
