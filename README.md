# UAS-Pemrograman-komputer-Aulia-Putri-Raffliana-09011182328004

Nama : Aulia Putri Raffliana

Kelas : SK1A

Nim : 09011182328004

UJIAN AKHIR SEMESTER PEMROGRAMAN KOMPUTER

Soal 1.
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.print("Masukkan harga barang: ");
        double harga = input.nextDouble();

        System.out.print("Masukkan jumlah pembelian: ");
        int jumlah = input.nextInt();

        double diskon = 0;
        if (jumlah >= 5 && jumlah <= 10) {
            diskon = 0.05;
        } else if (jumlah >= 11 && jumlah <= 20) {
            diskon = 0.1;
        } else if (jumlah > 20) {
            diskon = 0.2;
        }

        double totalHarga = harga * jumlah;
        double totalDiskon = totalHarga * diskon;
        double hargaSetelahDiskon = totalHarga - totalDiskon;

        System.out.println("Total harga setelah diskon: $" + hargaSetelahDiskon);
    }
}
