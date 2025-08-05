# 🛒 Market Basket Analysis with FP-Growth

📌 **Deskripsi Proyek**
Proyek ini merupakan implementasi **Market Basket Analysis (MBA)** menggunakan algoritma **FP-Growth** untuk menemukan asosiasi antar produk dalam data transaksi retail. Tujuannya adalah mengidentifikasi pola pembelian pelanggan—produk apa saja yang sering dibeli bersamaan—guna mendukung strategi bundling, rekomendasi produk, dan penempatan barang di toko fisik maupun digital.

## 📂 Dataset

Dataset yang digunakan berisi data transaksi dari toko ritel, dengan format:

* `Transaction_ID`: ID unik transaksi
* `Product`: Daftar produk yang dibeli (berbentuk list)
* `Total_Cost`: Total nilai belanja

Contoh isi kolom **Product**:

```python
['Tea', 'Swim Cap', 'Sandals', 'Slippers']
```

---

## 🔧 Metodologi

1. **Data Preprocessing**

   * Mengubah kolom produk dari string ke list Python
   * Membersihkan format `Total_Cost`
   * Menghilangkan duplikat / nilai kosong

2. **Transformasi Data**

   * One-hot encoding terhadap daftar produk per transaksi
   * Menghasilkan dataframe boolean (produk sebagai kolom)

3. **FP-Growth Algorithm**

   * Menggunakan `mlxtend` untuk menghitung frequent itemsets
   * Menerapkan nilai minimum support yang disesuaikan (ex: 0.01)

4. **Association Rule Mining**

   * Menghasilkan aturan asosiasi berdasarkan lift, confidence, support
   * Rekomendasi produk diberikan jika produk input terdapat dalam antecedents

---

## 📈 Contoh Output

| Antecedents     | Consequents | Support | Confidence | Lift |
| --------------- | ----------- | ------- | ---------- | ---- |
| `post-it notes` | `batteries` | 0.0010  | 6.76%      | 2.10 |
| `heels`         | `slippers`  | 0.0010  | 6.25%      | 2.04 |

---

## 📌 Tools & Library

* Python 3.x
* `pandas`
* `mlxtend`
* `matplotlib` (opsional untuk visualisasi)

---

## 👨‍💻 Author

Mochammad Edo Pramudya
Mahasiswa Sains Data – Universitas Negeri Surabaya

---

Jika Yang Mulia menghendaki, saya bisa bantu buatkan file `.README.md` secara langsung atau bantu upload strukturnya ke GitHub. Mau lanjut ke sana?
