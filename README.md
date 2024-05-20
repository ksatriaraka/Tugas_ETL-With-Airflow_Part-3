# Tugas_ETL-With-Airflow_Part-3
Tugas ETL with Airflow part 3

# PENJELASAN langkah-langkah CODE DARI 2 FILE DI ATAS
## op_mysql.py
1. Pertama, impor beberapa modul yang dibutuhkan, yaitu datetime dari Python standard library, DAG, EmptyOperator, dan MySqlOperator dari pustaka airflow, serta mysql dari provider MySQL untuk Airflow.
2. Kemudian, definisikan sebuah DAG (Directed Acyclic Graph) dengan dag_id "op_mysql_example", start_date tanggal bulan Mei tahun 2024, catchup diatur menjadi False, dan schedule_interval sebulan.
3. Buat sebuah EmptyOperator dengan task_id "start" sebagai task awal.
4. Buat sebuah MySqlOperator dengan task_id "create_new_table" untuk membuat tabel baru "students" di basis data MySQL.
5. Buat sebuah MySqlOperator lainnya dengan task_id "insert_data" untuk menginput data ke tabel "students".
6. Buat sebuah EmptyOperator lagi dengan task_id "end" sebagai task terakhir.
7. Gunakan operator >> untuk menghubungkan antara task-task tersebut, sehingga membentuk sebuah workflow.
## op_postgresql.py
1. Pertama, impor beberapa modul yang dibutuhkan, yaitu datetime dari Python standard library, DAG, EmptyOperator, dan PostgresOperator dari pustaka airflow, serta postgres dari provider PostgreSQL untuk Airflow.
2. Kemudian, definisikan sebuah DAG (Directed Acyclic Graph) dengan dag_id "op_postgres_example", start_date tanggal bulan Mei tahun 2024, catchup diatur menjadi False, dan schedule_interval setiap minggu.
3. Buat sebuah EmptyOperator dengan task_id "start" sebagai task awal.
4. Buat sebuah PostgresOperator dengan task_id "create_pet_table" untuk membuat tabel baru "pet" di basis data PostgreSQL.
5. Buat sebuah PostgresOperator lainnya dengan task_id "populate_pet_table" untuk memasukkan data ke tabel "pet".
6. Buat sebuah EmptyOperator lagi dengan task_id "end" sebagai task terakhir.
7. Gunakan operator >> untuk menghubungkan antara task-task tersebut, sehingga membentuk sebuah workflow.
