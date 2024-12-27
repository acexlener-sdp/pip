###
Ketika Anda menggunakan pip untuk menginstal paket Python, Anda mungkin mengalami kesalahan <strong>'externally-managed-environment'</strong>. Kesalahan ini terjadi karena lingkungan Python Anda “dikelola secara eksternal” oleh manajer paket, yang mencegah penggunaan pip secara langsung untuk instalasi di seluruh sistem untuk menghindari konflik atau masalah.
###
Kesalahan: Lingkungan yang Dikelola Secara Eksternal Terpecahkan<br>
Kesalahan: <strong>externally-managed-environment</strong> terjadi ketika manajer paket mengelola lingkungan Python, yang mencegah penggunaan pip secara langsung. Hal ini dapat diatasi dengan menggunakan lingkungan virtual:
# 2 Cara untuk Mengatasi Kesalahan: <strong>externally-managed-environment</strong>

### 1. Gunakan Lingkungan Virtual
 <p>
   Salah satu cara untuk mengatasinya error: externally-managed-environmentadalah dengan membuat folder lingkungan virtual di jalur root Anda. Dengan membuat dan menggunakan lingkungan virtual, Anda melewati sistem Python sepenuhnya, yang memungkinkan Anda untuk menginstal dan mengelola paket secara bebas tanpa memengaruhi instalasi Python di seluruh sistem .
 </p>


```bash
python3 -m venv ~/py_envs
source ~/py_envs/bin/activate
python3 -m pip install xyz
```


### 2. Install Paksa
<p>
  Pilihan kedua adalah melakukan instalasi paksa. Penggunaannya <strong>--break-system-packages</strong> melewati perlindungan ini, sehingga Anda dapat menginstal paket secara langsung ke lingkungan Python di seluruh sistem.
</p>
<br>
<p>
  Untuk melakukan hal ini, tambahkan <strong>--break-system-packages</strong> di akhir pip, misalnya:
</p>
<br>

```bash
pip install xyz --break-system-packages.
```
