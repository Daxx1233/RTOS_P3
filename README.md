# Praktikum RTOS - SEMESTER 5 (3 Teknik Komputer A)
- Triyas Rahmadiyanti (3222600001)
- Duta Fithra Qolby (3222600003)
# Task 3 - 
## Deskripsi Projek
Berikut ini adalah alur dalam projek kali ini :
1. Inisialisasi dan Pengaturan Awal:
   -  HAL_Init(): Menginisialisasi library HAL (Hardware Abstraction Layer) untuk mengatur semua periferal dan timer sistem.
   -  SystemClock_Config(): Mengatur sistem clock untuk menggunakan osilator internal (HSI) dan mengatur pembagi clock untuk CPU dan bus.
   -  MX_GPIO_Init(): Menginisialisasi port GPIO untuk mengontrol LED (LED hijau dan merah) sebagai output.
2. Setup RTOS (Real-Time Operating System):
   - osKernelInitialize(): Menyiapkan kernel RTOS agar siap menjalankan tugas (task).
   - Pembuatan Tugas (Task): Program membuat tiga tugas:
   - defaultTask: Tugas default yang hanya melakukan loop dengan penundaan 1 ms.
   - FlashGreenLedTa: Tugas untuk menyalakan dan mematikan LED hijau.
   - FlashRedLedTask: Tugas untuk menyalakan dan mematikan LED merah. Setiap tugas diberikan identitas dan atribut seperti nama, ukuran stack, dan prioritas. Tugas LED merah diberi prioritas lebih tinggi dari LED hijau.
3. Implementasi Tugas:
   - StartDefaultTask: Tugas default yang hanya menjalankan loop dengan penundaan waktu (tidak melakukan operasi khusus).
   - FlashGreenTask:
     > Menyalakan indikator LED hijau.
     > Mematikan LED hijau utama.
     > Mengedipkan LED hijau sebanyak 80 kali dengan penundaan 25 ms.
     > Mematikan indikator LED hijau.
     > Menunggu selama 6 detik sebelum mengulang proses.
    - FlashRedTask:
      >  Menyalakan indikator LED merah.
      > Mematikan LED merah utama.
      >  Mengedipkan LED merah 10 kali dengan penundaan 25 ms.
      > Mematikan indikator LED merah.
      > Menunggu selama 1,5 detik sebelum mengulang proses.
5. Penanganan Error:
   - Error_Handler(): Fungsi yang dijalankan jika terjadi error. Fungsi ini menghentikan program dengan menonaktifkan interrupt dan masuk ke loop tak terbatas.
- Alur Program: Program mengatur clock sistem, inisialisasi port GPIO, dan mempersiapkan kernel RTOS.
- Program membuat tiga tugas:
  1. Tugas default yang hanya menjalankan loop.
  2. Tugas untuk mengedipkan LED hijau dengan pola tertentu.
  3. Tugas untuk mengedipkan LED merah dengan pola berbeda dan prioritas lebih tinggi.
  > Tugas-tugas ini berjalan secara bersamaan di bawah pengaturan RTOS, dengan tugas LED merah memiliki prioritas lebih tinggi daripada tugas LED hijau.
Projek ini merupakan struktur dasar program embedded yang menggunakan FreeRTOS untuk mengelola beberapa tugas secara bersamaan, dimana setiap tugas menangani komponen atau fungsi berbeda secara independen.
# Gambar Hardware
![WhatsApp Image 2024-10-17 at 20 51 19](https://github.com/user-attachments/assets/bfa2660c-a293-443e-9db4-8b8901da81e8)
# Video Hardware
Tampak samping

https://github.com/user-attachments/assets/85de8fd0-4b8c-4aac-8c0e-cda337ef9dfe


Tampak depan

https://github.com/user-attachments/assets/ab8f3dcd-3970-4bce-97fe-ab8f60a9c090





  
