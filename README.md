# Project1
Nama Kelompok - Data Divers
AMINUDIN
SENDHI A RAHMANSYAH
HANIFAH RIZKY MUFIIDAH
M QORI RAMADHAN NASUTION
HAMZAH AL FARISI
Tentang
Proyek ini, yang dikembangkan oleh tim Data Divers, adalah pipeline ETL (Extract, Transform, Load) yang dirancang untuk mengekstrak data dari database marketplace, mengubahnya ke dalam format yang sesuai, dan memuatnya ke dalam data warehouse untuk analisis lebih lanjut.

Fitur Utama
Ekstraksi Data: Menghubungkan ke database produksi marketplace untuk mengekstrak data yang relevan.
Transformasi Data: Memproses dan mengubah data yang diekstrak agar sesuai dengan skema data warehouse.
Pemuatan Data: Memuat data yang telah diubah ke dalam data warehouse, khususnya ke dalam tabel dim_orders_faris.
Otomatisasi: Seluruh proses ETL diotomatisasi dan dapat dijalankan dengan satu skrip.
Komponen
main.py: Skrip utama yang mengatur proses ETL.
config.json: File konfigurasi yang berisi detail koneksi database.
query/query.sql: Query SQL untuk mengekstrak data dari database sumber.
query/dwh_design.sql: Skrip SQL untuk membuat tabel yang diperlukan di data warehouse.
requirements.txt: Daftar dependensi Python yang diperlukan untuk proyek ini.
Cara Kerja
Konfigurasi: Skrip membaca detail koneksi database dari config.json.
Ekstraksi Data: Menjalankan query SQL di query/query.sql untuk mengekstrak data dari database sumber.
Transformasi Data: Mengubah data yang diekstrak menggunakan pandas.
Pemuatan Data: Membuat tabel yang diperlukan di data warehouse menggunakan query/dwh_design.sql dan memuat data yang telah diubah ke dalamnya.
Proyek ini bertujuan untuk menyederhanakan proses pengambilan dan transformasi data, sehingga lebih mudah untuk menganalisis dan mendapatkan wawasan dari data marketplace.

Getting Started
Prerequisites
Ensure you have the following installed:

Python 3.7
pip (Python package installer)
Installation
Clone the repository:

git clone https://github.com/hotspoon/project_1
cd project_1
Create a virtual environment:

python3 -m venv devEnv
Activate the virtual environment:

On Windows:
.\devEnv\Scripts\activate
On macOS/Linux:
source devEnv/bin/activate
Install the required packages:

pip install -r requirements.txt
Configuration
Update the [config.json] file with your database credentials if necessary.
Running the ETL Process
Run the ETL script:
python main.py
This will connect to the data source and data warehouse, execute the queries, and ingest the data into the data warehouse.
