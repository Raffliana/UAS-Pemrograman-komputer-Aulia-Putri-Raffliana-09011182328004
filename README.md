# UAS-Pemrograman-komputer-Aulia-Putri-Raffliana-09011182328004
Nama : Aulia Putri Raffliana
Kelas : SK1A
Nim : 09011182328004
UJIAN AKHIR SEMESTER PEMROGRAMAN KOMPUTER
1. Diskon
   


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


2. Autentikasi
import java.util.Scanner;

public class AutentikasiPengguna {
    public static void main(String[] args) {
        // Menentukan nilai username dan password yang benar
        String usernameBenar = "Raffliana";
        String passwordBenar = "amersayang";

        // Membaca input username dan password dari pengguna
        Scanner scanner = new Scanner(System.in);
        System.out.print("Masukkan username: ");
        String username = scanner.nextLine();
        System.out.print("Masukkan password: ");
        String password = scanner.nextLine();

        // Memeriksa apakah username dan password sesuai dengan nilai yang telah ditentukan
        if (username.equals(usernameBenar) && password.equals(passwordBenar)) {
            System.out.println("Autentikasi Berhasil");
        } else {
            System.out.println("Autentikasi Gagal");
        }
    }
}


3. Fibonacci
   import java.util.Scanner;

public class FibonacciSeries {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.print("Masukkan jumlah suku Fibonacci yang ingin ditampilkan: ");
        int n = input.nextInt();

        System.out.println("Deret Fibonacci hingga suku ke-" + n + ":");
        for (int i = 1; i <= n; i++) {
            System.out.print(fibonacci(i) + " ");
        }
    }

    public static int fibonacci(int n) {
        if (n <= 1) {
            return n;
        } else {
            return fibonacci(n - 1) + fibonacci(n - 2);
        }
    }
}


4. Faktorisasi
import java.util.Scanner;

public class Faktorisasi {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.print("Masukkan bilangan bulat positif: ");
        int bilangan = input.nextInt();
        
        System.out.print("Faktorisasi " + bilangan + ": ");
        faktorisasi(bilangan);
    }
    
    public static void faktorisasi(int bilangan) {
        for (int i = 2; i <= bilangan; i++) {
            while (bilangan % i == 0) {
                System.out.print(i);
                bilangan /= i;
                
                if (bilangan != 1) {
                    System.out.print(" * ");
                }
            }
        }
    }
}


5. Kalkulator
import java.util.Scanner;

public class Kalkulator {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        double num1, num2, result;
        char operator;

        System.out.print("Masukkan angka pertama: ");
        num1 = input.nextDouble();

        System.out.print("Masukkan operator (+, -, *, /): ");
        operator = input.next().charAt(0);

        System.out.print("Masukkan angka kedua: ");
        num2 = input.nextDouble();

        switch (operator) {
            case '+':
                result = tambah(num1, num2);
                System.out.println(num1 + " + " + num2 + " = " + result);
                break;
            case '-':
                result = kurang(num1, num2);
                System.out.println(num1 + " - " + num2 + " = " + result);
                break;
            case '*':
                result = kali(num1, num2);
                System.out.println(num1 + " * " + num2 + " = " + result);
                break;
            case '/':
                result = bagi(num1, num2);
                System.out.println(num1 + " / " + num2 + " = " + result);
                break;
            default:
                System.out.println("Operator yang dimasukkan tidak valid.");
                break;
        }
    }

    public static double tambah(double num1, double num2) {
        return num1 + num2;
    }

    public static double kurang(double num1, double num2) {
        return num1 - num2;
    }

    public static double kali(double num1, double num2) {
        return num1 * num2;
    }

    public static double bagi(double num1, double num2) {
        return num1 / num2;
    }
}


6. Palindrom
import java.util.Scanner;

public class PalindromeChecker {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Masukkan kata atau frase: ");
        String input = scanner.nextLine();

        if (isPalindrome(input)) {
            System.out.println(input + " adalah palindrom.");
        } else {
            System.out.println(input + " bukan palindrom.");
        }
    }

    public static boolean isPalindrome(String input) {
        // Menghapus spasi dan mengubah semua huruf menjadi huruf kecil
        input = input.replaceAll("\\s+", "").toLowerCase();

        int left = 0;
        int right = input.length() - 1;

        while (left < right) {
            if (input.charAt(left) != input.charAt(right)) {
                return false;
            }
            left++;
            right--;
        }

        return true;
    }
}


7. Perpustakaan Buku
public class Buku{
    private String judul;
    private String penulis;
    private int tahunTerbit;
    private boolean tersedia;
    // inisialisasi buku
    public Buku(String judul, String penulis, int tahunTerbit) {
        this.judul = judul;
        this.penulis = penulis;
        this.tahunTerbit = tahunTerbit;
        this.tersedia = true;
    }
    // menampilkan informasi buku
    public void tampilkanInfoBuku() {
        System.out.println("Judul: " + judul);
        System.out.println("Penulis: " + penulis);
        System.out.println("Tahun Terbit: " + tahunTerbit);
        System.out.println("Status: " + (tersedia ? "Tersedia" : "Tidak Tersedia"));
    }
    // untuk meminjam buku
    public void pinjamBuku() {
        if (tersedia) {
            System.out.println("Buku tersedia & dapat dipinjam.");
            tersedia = false;
        } else {
            System.out.println("Buku tidak tersedia.");
        }
    }
    public static void main(String[] args) {
        Buku buku1 = new Buku("Hujan", "Tereliye", 2012);
        // menampilkan informasi buku sebelum dipinjam
        System.out.println("Informasi buku sebelum dipinjam:");
        buku1.tampilkanInfoBuku();
        // meminjam buku
        buku1.pinjamBuku();
        // menampilkan informasi buku setelah dipinjam
        System.out.println("\nInformasi buku setelah dipinjam:");
        buku1.tampilkanInfoBuku();
    }
}


8. Akun
public class Akun {

    private String username;
    private String password;
    private boolean aktif;

    // inisialisasi atribut akun
    public Akun(String username, String password) {
        this.username = username;
        this.aktif = false;
    }

    // menampilkan informasi akun
    public void tampilkanInfoAkun() {
        System.out.println("Username: " + username);
        System.out.println("Status: " + (aktif ? "Aktif" : "Nonaktif"));
    }

    // mengaktifkan akun
    public void aktifkanAkun() {
        if (!aktif) {
            System.out.println("Akun berhasil diaktifkan.");
            aktif = true;
        } else {
            System.out.println("Akun sudah aktif.");
        }
    }

    // menonaktifkan akun
    public void nonaktifkanAkun() {
        if (aktif) {
            System.out.println("Akun berhasil dinonaktifkan.");
            aktif = false;
        } else {
            System.out.println("Akun sudah nonaktif.");
        }
    }

    public static void main(String[] args) {
        // membuat objek akun
        Akun akun1 = new Akun("Raffliana", "Amersayang");

        // menampilkan informasi akun sebelum diaktifkan
        System.out.println("Informasi akun sebelum diaktifkan:");
        akun1.tampilkanInfoAkun();

        // mengaktifkan akun
        akun1.aktifkanAkun();

        // menampilkan informasi akun setelah diaktifkan
        System.out.println("\nInformasi akun setelah diaktifkan:");
        akun1.tampilkanInfoAkun();

        // menonaktifkan akun
        akun1.nonaktifkanAkun();

        // menampilkan informasi akun setelah dinonaktifkan
        System.out.println("\nInformasi akun setelah dinonaktifkan:");
        akun1.tampilkanInfoAkun();
    }
}


9. Stack

import java.util.Stack;

public class CheckParentheses {
    public static boolean checkParentheses(String expression) {
        Stack<Character> stack = new Stack<>();

        for (int i = 0; i < expression.length(); i++) {
            char c = expression.charAt(i);

            if (c == '(') {
                stack.push(c);
            } else if (c == ')') {
                if (stack.isEmpty() || stack.peek() != '(') {
                    return false;
                } else {
                    stack.pop();
                }
            }
        }

        return stack.isEmpty();
    }

    public static void main(String[] args) {
        String expression1 = "((2 + 3) * 5)";
        String expression2 = "((2 + 3) * 5))";
        String expression3 = "((2 + 3) * 5";

        System.out.println("Expression 1: " + checkParentheses(expression1));
        System.out.println("Expression 2: " + checkParentheses(expression2));
        System.out.println("Expression 3: " + checkParentheses(expression3));
    }
}

