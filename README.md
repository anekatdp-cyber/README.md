# 🚀 OOP Dart - Polimorfisme & Abstraksi

## 📌 Deskripsi
Repository ini berisi ringkasan dan contoh implementasi konsep:
- Polimorfisme
- Abstraksi
- Interface
- Static Method

Menggunakan bahasa pemrograman Dart.

---

## 🎯 Tujuan
Memahami dan mengimplementasikan:
- Polimorfisme (Inheritance)
- Abstract Class
- Interface (implements)
- Static Method

---

## 🧠 1. Polimorfisme

### 📌 Pengertian
Polimorfisme adalah kemampuan objek untuk memiliki banyak bentuk.

### 📌 Contoh
Satu method → hasil berbeda tergantung objek.

```dart
class Hewan {
  void bersuara() {
    print("Hewan bersuara");
  }
}

class Kucing extends Hewan {
  @override
  void bersuara() => print("Meong");
}

class Anjing extends Hewan {
  @override
  void bersuara() => print("Guk Guk");
}
📌 Manfaat
Kode fleksibel
Mudah dikembangkan
Mengurangi duplikasi
🔍 Operator is dan as
if (hewan is Kucing) {
  print("Ini kucing");
}

(hewan as Kucing).bersuara();
🧠 2. Abstraksi
📌 Abstract Class
abstract class Kendaraan {
  void jalan();
}
📌 Implementasi
class Mobil extends Kendaraan {
  @override
  void jalan() {
    print("Mobil berjalan");
  }
}
🔌 Interface (implements)
class Mesin {
  void nyala() {}
}

class Motor implements Mesin {
  @override
  void nyala() {
    print("Mesin motor nyala");
  }
}
⚖️ Perbedaan extends vs implements
extends	implements
Turunan class	Implementasi interface
Bisa pakai method parent	Wajib override semua method
Relasi "is-a"	Kontrak
🧮 Static Method
class MathUtil {
  static int tambah(int a, int b) {
    return a + b;
  }
}
💼 Contoh Kasus
💳 Sistem Pembayaran
abstract class Pembayaran {
  void bayar();
}
🔷 Sistem Geometri
abstract class Bentuk {
  double hitungLuas();
}
