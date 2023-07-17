Output:
Method dari class induk
x=3
Method dari class turunan
nilai x=4
nilai y=5

Dalam kode yang diberikan, class turunan mewarisi semua behavior (method) dari class induk dasar. Berikut adalah behavior yang diturunkan oleh class induk dasar ke class turunan:
- public int getX(): Method ini mengembalikan nilai x dari objek dasar.
- public void tampilkanInformasi(): Method ini mencetak informasi "Method dari class induk" dan nilai x dari objek dasar.
Selain itu, class turunan juga memiliki behavior tambahan yang ditentukan di dalamnya sendiri:
- public void tampilkanInformasi(): Method ini menggantikan method tampilkanInformasi() dari class induk dan mencetak informasi "Method dari class turunan", nilai x dari objek dasar (diperoleh melalui pemanggilan super.getX()), dan nilai y dari objek turunan.
Dalam metode main(), instance a dari class dasar dan instance b dari class turunan dibuat dan method tampilkanInformasi() dipanggil pada masing-masing objek. Untuk objek a, method tampilkanInformasi() dari class dasar akan dipanggil, sedangkan untuk objek b, method tampilkanInformasi() yang diwarisi dari class dasar akan digantikan oleh method tampilkanInformasi() yang didefinisikan di dalam class turunan.

Dalam kode yang diberikan, class turunan melakukan overriding (menggantikan) method tampilkanInformasi() dari class induk dasar. Oleh karena itu, behavior (method) yang dioverride oleh class turunan adalah:
public void tampilkanInformasi(): Method ini dioverride oleh class turunan. Method ini menggantikan implementasi method tampilkanInformasi() dari class dasar. Dalam class turunan, method ini mencetak informasi "Method dari class turunan", nilai x dari objek dasar (diperoleh melalui pemanggilan super.getX()), dan nilai y dari objek turunan.

===================================================================

Output:
Luas bujur sangkar adalah:16
Keliling bujur sangkar adalah:16
Luas persegi adalah:8.0
Keliling persegi:12

Dalam kode yang diberikan, tidak ada kelas dengan nama "bangun2D". Yang ada adalah kelas "bentuk2D". Oleh karena itu, kita akan mengasumsikan bahwa "bangun2D" adalah kesalahan penulisan dan sebenarnya dimaksudkan "bentuk2D".
Dalam kelas "bentuk2D", terdapat dua metode abstrak yang harus diimplementasikan oleh kelas anak yaitu "bujurSangkar" dan "persegiPanjang". Metode abstrak tersebut adalah:
- cetakLuas(): Metode ini digunakan untuk mencetak luas bentuk 2D.
- cetakKeliling(): Metode ini digunakan untuk mencetak keliling bentuk 2D.
Dalam kelas "bujurSangkar", kedua metode tersebut diimplementasikan sebagai berikut:
public void cetakLuas() {
    luas = sisi * sisi;
    System.out.println("Luas bujur sangkar adalah:" + luas);
}

public void cetakKeliling() {
    keliling = 4 * sisi;
    System.out.println("Keliling bujur sangkar adalah:" + keliling);
}
Dalam kelas "persegiPanjang", kedua metode tersebut diimplementasikan sebagai berikut:
public void cetakLuas() {
    luas = panjang * lebar;
    System.out.println("Luas persegi adalah:" + luas);
}

public void cetakKeliling() {
    keliling = 2 * (panjang + lebar);
    System.out.println("Keliling persegi:" + keliling);
}

Tidak, kode tersebut tidak dapat dikompilasi. Kita tidak dapat membuat objek dari kelas abstract secara langsung menggunakan operator new.
Kelas abstract sendiri tidak dapat diinstansiasi, yang berarti kita tidak dapat membuat objek langsung dari kelas abstract tersebut. Tujuan kelas abstract adalah untuk digunakan sebagai kerangka atau template untuk kelas-kelas turunannya.
Kelas abstract memiliki setidaknya satu metode abstrak yang tidak memiliki implementasi. Oleh karena itu, tujuan utama kelas abstract adalah untuk menjadi superclass atau kontrak yang mengharuskan kelas-kelas turunannya untuk mengimplementasikan metode-metode abstrak tersebut.
Sebagai gantinya, kita harus membuat objek dari kelas yang mengimplementasikan kelas abstract tersebut. Dalam contoh ini, kita dapat membuat objek dari kelas "bujurSangkar" atau "persegiPanjang" yang merupakan turunan dari kelas "bentuk2D". Contohnya seperti ini:
bentuk2D objAbstract = new bujurSangkar(5);
objAbstract.cetakLuas();
objAbstract.cetakKeliling();
Dengan membuat objek dari kelas turunan, kita dapat menggunakan polimorfisme untuk memanggil metode-metode yang diwarisi dari kelas abstract dan mengimplementasikan fungsionalitas khusus untuk setiap kelas turunan tersebut.

====================================================================

Output:
Mesin cuci Toshiba dihidupkan
Mesin cuci Toshiba sudahhidup
Mesin cuci Toshiba dimatikan
Mesin cuci Toshibakeadaan mati

Berikut adalah penjelasan jalannya program berdasarkan pemanggilan method pada class MainMesin serta output program yang terjadi:
- Objek Toshiba dari kelas mesinCuci diciptakan dengan parameter "Mesin cuci Toshiba".
- Method hidupkanMesin() dipanggil pada objek Toshiba. Karena isHidup() mengembalikan nilai false (default), maka kondisi else akan dieksekusi. hidup diatur menjadi true dan output yang dihasilkan adalah "Mesin cuci Toshiba dihidupkan".
- Method hidupkanMesin() dipanggil lagi pada objek Toshiba. Karena isHidup() mengembalikan nilai true, maka kondisi if akan dieksekusi. Output yang dihasilkan adalah "Mesin cuci Toshiba sudahhidup".
- Method matikanMesin() dipanggil pada objek Toshiba. Karena isHidup() mengembalikan nilai true, maka kondisi if akan dieksekusi. hidup diatur menjadi false dan output yang dihasilkan adalah "Mesin cuci Toshiba dimatikan".
- Method matikanMesin() dipanggil lagi pada objek Toshiba. Karena isHidup() mengembalikan nilai false, maka kondisi else akan dieksekusi. hidup diatur menjadi true dan output yang dihasilkan adalah "Mesin cuci Toshiba keadaan mati".
Output:
Mesin cuci Toshiba dihidupkan
Mesin cuci Toshiba sudahhidup
Mesin cuci Toshiba dimatikan
Mesin cuci Toshibakeadaan mati
Demikianlah penjelasan tentang jalannya program berdasarkan pemanggilan method pada class MainMesin dan output program yang terjadi.