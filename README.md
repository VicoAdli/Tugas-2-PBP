1
Buat virtual environment dengan python -m venv env setelah berhasil cd pada command prompt ke direktori tujuan
Lalu aktifkan venv dengan env\Scripts\activate.bat
Buat requirements.txt untuk menambahkan dependencies seperti django, gunicorn, whitenoise, psycopg2-binary, requests, urllib3 lalu pasang dengan pip install -r requirements.txt
Saya buat proyek Django baru dengan perintah django-admin startproject pbp_project .
Menambahkan "*" pada variabel ALLOWED_HOSTS di settings.py untuk keperluan deployment
Membuat aplikasi baru dengan python manage.py startapp main
Menambahkan "main" pada variabel INSTALLED_APPS di settings.py untuk keperluan pendaftaran aplikasi main
Membuat folder bernama templates di dalam direktori main dan membuat file main.html di dalam direktori templates. Isi file dengan nilai yang sesuai
Buka berkas models.py pada direktori aplikasi main dan isi dengan kode yang diperlukan
Membuat migrasi model dengan python manage.py makemigrations
Terapkan migrasi dengan python manage.py migrate
Buka berkas views.py yang terletak di dalam berkas aplikasi main dan isi dengan kode yang diperlukan
Buat berkas urls.py di dalam direktori main dan isi dengan kode yang diperlukan
Buka berkas urls.py di dalam direktori pbp_project dan isi dengan kode yang diperlukan
Jalankan server django dengan python manage.py runserver

2
Bagan request client ke web aplikasi berbasis Django beserta responnya akan bergantung pada interaksi antara client, URL routing (urls.py), views (views.py), models (models.py), dan berkas HTML.

[Client] --> [URLs.py] --> [Views.py] --> [Models.py] --> [HTML Template]
           <--           <--           <--             <--
           HTTP Request           Data Query          Data Rendering

Client: Membuat HTTP request untuk mengakses aplikasi.
URLs.py: Mengarahkan request ke view yang sesuai berdasarkan URL yang diterima.
Views.py: Memproses request, mengakses data dari model jika diperlukan, dan mengirim data ke template HTML.
Models.py: Menyimpan definisi data model (dalam hal ini, model 'Item').
HTML Template: Mengambil data yang dikirim oleh views dan merendernya ke dalam tampilan HTML yang dapat dilihat oleh client.

3
1. Virtual environment memungkinkan kita untuk mengisolasi dependensi proyek kita dari lingkungan Python sistem yang lebih besar.
2. Virtual environment memungkinkan kita untuk mengelola dependensi proyek kita dengan lebih baik.
3. Virtual environment membantu menjaga lingkungan Python sistem kita tetap bersih dan tidak tercampur dengan dependensi proyek.
4. Dengan menggunakan virtual environment, kita dapat mencatat dependensi proyek kita dalam sebuah berkas (seperti requirements.txt) sehingga kita atau orang lain dapat dengan mudah menginstal semua dependensi yang diperlukan pada lingkungan yang sama dan memastikan bahwa proyek berjalan dengan konsisten.

Secara teori, kita masih dapat membuat aplikasi web Django tanpa menggunakan virtual environment, tetapi ini akan menjadi praktik yang sangat tidak disarankan karena dapat menghasilkan berbagai masalah dan konflik dalam pengembangan proyek

4
MVC (Model-View-Controller) adalah paradigma yang memisahkan aplikasi menjadi tiga komponen utama: Model (data dan bisnis logic), View (tampilan pengguna), dan Controller (mengatur interaksi antara Model dan View). MVC umumnya digunakan dalam kerangka kerja seperti Ruby on Rails.

MVT (Model-View-Template) adalah varian Django dari MVC. Dalam MVT, Model masih mengacu pada data dan bisnis logic, View adalah logika yang mengatur tampilan, dan Template adalah bagian yang menangani tampilan HTML. Django memanfaatkan konsep Template yang kuat.

MVVM (Model-View-ViewModel) adalah paradigma yang digunakan dalam pengembangan aplikasi berbasis antarmuka pengguna (UI). Ini memisahkan Model (data), View (tampilan UI), dan ViewModel (logika untuk mengatur tampilan dan data). MVVM lebih sering digunakan dalam pengembangan aplikasi seluler atau berbasis desktop.

Perbedaan utama adalah dalam cara mereka mengatur komponen-komponen utama aplikasi dan peran masing-masing komponen. Django mengikuti paradigma MVT yang merupakan variasi dari MVC.