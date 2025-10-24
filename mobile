import 'package:flutter/material.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      home: Scaffold(
        appBar: AppBar(
          title: const Text('Desain Widget Kombinasi'),
          backgroundColor: Colors.blueAccent,
        ),
        // Gunakan Center dan Padding agar kartu tidak menempel di tepi layar
        body: Center(
          child: Padding(
            padding: const EdgeInsets.all(16.0),
            child: DestinationCard(), // Ini adalah widget kustom kita
          ),
        ),
        backgroundColor: Colors.grey[100],
      ),
    );
  }
}

// Ini adalah widget kustom yang menggabungkan semua elemen
class DestinationCard extends StatelessWidget {
  const DestinationCard({super.key});

  @override
  Widget build(BuildContext context) {
    return Card(
      elevation: 8.0,
      shape: RoundedRectangleBorder(
        borderRadius: BorderRadius.circular(15.0),
      ),
      clipBehavior: Clip.antiAlias, // Untuk memotong gambar agar sesuai border radius
      child: Container(
        // ======== WIDGET COLUMN (Layout Utama) ========
        // Column digunakan untuk menyusun elemen secara vertikal
        // (Gambar -> Baris Judul/Rating -> Baris Tombol)
        child: Column(
          mainAxisSize: MainAxisSize.min, // Agar ukuran Column mengikuti konten
          crossAxisAlignment: CrossAxisAlignment.start,
          children: [
            // ======== 1. WIDGET IMAGE ========
            // Menampilkan gambar dari internet
            Image.network(
              'https://images.unsplash.com/photo-1507525428034-b723cf961d3e?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80',
              height: 200,
              width: double.infinity, // Lebar penuh sesuai kartu
              fit: BoxFit.cover,
            ),

            // Padding untuk konten teks di bawah gambar
            Padding(
              padding: const EdgeInsets.all(16.0),
              child: Column(
                crossAxisAlignment: CrossAxisAlignment.start,
                children: [
                  // ======== WIDGET ROW (Baris Judul & Rating) ========
                  // Row digunakan untuk meletakkan elemen secara horizontal
                  // (Teks Judul di kiri, Icon & Teks Rating di kanan)
                  Row(
                    mainAxisAlignment: MainAxisAlignment.spaceBetween,
                    children: [
                      // ======== 2. WIDGET TEXT (Judul) ========
                      Text(
                        'Pantai Tropis',
                        style: TextStyle(
                          fontSize: 22.0,
                          fontWeight: FontWeight.bold,
                        ),
                      ),
                      
                      // Row lain di dalam Row untuk rating
                      Row(
                        children: [
                          // ======== 3. WIDGET ICON (Bintang) ========
                          Icon(
                            Icons.star,
                            color: Colors.orange,
                            size: 20,
                          ),
                          SizedBox(width: 4),
                          // ======== WIDGET TEXT (Rating) ========
                          Text(
                            '4.8',
                            style: TextStyle(fontSize: 16),
                          ),
                        ],
                      ),
                    ],
                  ),

                  const SizedBox(height: 8.0),

                  // ======== WIDGET TEXT (Deskripsi Lokasi) ========
                  Text(
                    'Lokasi tersembunyi di selatan pulau. Tempat sempurna untuk bersantai dan menikmati matahari terbenam.',
                    style: TextStyle(
                      fontSize: 14.0,
                      color: Colors.grey[700],
                    ),
                  ),

                  const SizedBox(height: 20.0),

                  // ======== WIDGET ROW (Baris Tombol Aksi) ========
                  // Row digunakan untuk meletakkan dua tombol secara horizontal
                  Row(
                    mainAxisAlignment: MainAxisAlignment.spaceBetween,
                    children: [
                      // ======== 4. WIDGET BUTTON (ElevatedButton + Icon + Text) ========
                      ElevatedButton.icon(
                        onPressed: () {
                          // Aksi ketika tombol ditekan
                        },
                        icon: Icon(Icons.map_outlined), // Icon di tombol
                        label: Text('Lihat Peta'), // Teks di tombol
                        style: ElevatedButton.styleFrom(
                          backgroundColor: Colors.blueAccent,
                          foregroundColor: Colors.white,
                          shape: RoundedRectangleBorder(
                            borderRadius: BorderRadius.circular(10),
                          ),
                        ),
                      ),

                      // ======== WIDGET BUTTON (OutlinedButton + Icon) ========
                      OutlinedButton.icon(
                        onPressed: () {
                          // Aksi ketika tombol ditekan
                        },
                        icon: Icon(Icons.share), // Icon di tombol
                        label: Text('Bagikan'), // Teks di tombol
                        style: OutlinedButton.styleFrom(
                          foregroundColor: Colors.blueAccent,
                          side: BorderSide(color: Colors.blueAccent),
                          shape: RoundedRectangleBorder(
                            borderRadius: BorderRadius.circular(10),
                          ),
                        ),
                      ),
                    ],
                  ),
                ],
              ),
            ),
          ],
        ),
      ),
    );
  }
}
