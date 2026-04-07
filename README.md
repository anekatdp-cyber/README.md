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

void main() {
  print("=== POLIMORFISME ===");

  List<Hewan> daftarHewan = [
    Kucing(),
    Anjing(),
    Burung(),
  ];

  for (var h in daftarHewan) {
    h.bersuara();
  }

  print("\n=== OPERATOR is & as ===");

  Hewan hewan = Kucing();

  if (hewan is Kucing) {
    print("Objek adalah Kucing");
  }

  (hewan as Kucing).bersuara();

  print("\n=== ABSTRAKSI ===");

  Kendaraan mobil = Mobil();
  mobil.jalan();

  print("\n=== INTERFACE ===");

  Motor motor = Motor();
  motor.nyala();

  print("\n=== STATIC METHOD ===");
  print("Hasil tambah: ${MathUtil.tambah(5, 3)}");

  print("\n=== SISTEM PEMBAYARAN ===");

  List<Pembayaran> metodeBayar = [
    TransferBank(),
    EWallet(),
  ];

  for (var bayar in metodeBayar) {
    bayar.bayar();
  }

  print("\n=== SISTEM GEOMETRI ===");

  Bentuk persegi = Persegi(4);
  print("Luas Persegi: ${persegi.hitungLuas()}");
}

// ================================
// POLIMORFISME
// ================================

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

class Burung extends Hewan {
  @override
  void bersuara() => print("Cuit Cuit");
}

// ================================
// ABSTRAKSI
// ================================

abstract class Kendaraan {
  void jalan();
}

class Mobil extends Kendaraan {
  @override
  void jalan() {
    print("Mobil berjalan");
  }
}

// ================================
// INTERFACE
// ================================

class Mesin {
  void nyala() {}
}

class Motor implements Mesin {
  @override
  void nyala() {
    print("Mesin motor nyala");
  }
}

// ================================
// STATIC METHOD
// ================================

class MathUtil {
  static int tambah(int a, int b) {
    return a + b;
  }
}

// ================================
// PEMBAYARAN
// ================================

abstract class Pembayaran {
  void bayar();
}

class TransferBank extends Pembayaran {
  @override
  void bayar() {
    print("Bayar via Transfer Bank");
  }
}

class EWallet extends Pembayaran {
  @override
  void bayar() {
    print("Bayar via E-Wallet");
  }
}

// ================================
// GEOMETRI
// ================================

abstract class Bentuk {
  double hitungLuas();
}

class Persegi extends Bentuk {
  double sisi;

  Persegi(this.sisi);

  @override
  double hitungLuas() {
    return sisi * sisi;
  }
}
abstract class Pembayaran {
  void bayar();
}
🔷 Sistem Geometri
abstract class Bentuk {
  double hitungLuas();
}
