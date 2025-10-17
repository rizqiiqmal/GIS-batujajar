# Peta Jalan Wilayah (Data GeoJSON)

Repositori ini berisi data geospasial yang memetakan jaringan jalan, gang, dan jalur di sebuah wilayah di Indonesia. Data ini disimpan dalam satu file, `map.geojson`.

Data ini telah diuji dan dapat divisualisasikan dengan benar menggunakan *tool* online seperti **geojson.io**.

## 🗺️ Apa itu GeoJSON?

**GeoJSON** adalah format standar terbuka (bukan milik perusahaan tertentu) yang dirancang untuk merepresentasikan data geografis. Sederhananya, ini adalah cara untuk menulis data lokasi (seperti titik, garis, atau area) menggunakan format JSON (JavaScript Object Notation) yang ringan dan mudah dibaca manusia.

Karena formatnya yang universal, GeoJSON sangat populer dan didukung oleh hampir semua perangkat lunak GIS dan *library* pemetaan web (seperti Leaflet, Mapbox, dan Google Maps API).

##  Isi

File `map.geojson` ini adalah sebuah `FeatureCollection`, yang berarti file ini berisi *kumpulan* dari berbagai fitur geografis.

* **Tipe Geometri:** Setiap fitur di dalamnya menggunakan tipe geometri `LineString` (garis yang menghubungkan banyak titik koordinat).
* **Makna:** Setiap `LineString` merepresentasikan sebuah segmen jalan, gang, atau jalur.

Berdasarkan data, contoh jalan yang terpetakan meliputi:

* **Jalan Utama:** 
* Berdasarkan file `batujajar.geojson` (9 fitur `LineString`):
  * Semua fitur memiliki properti `highway: residential` — dataset ini hanya memetakan jalan perumahan.
  * Tipe geometri: `LineString`.
  * Properti nama jalan, `surface`, atau informasi akses kendaraan (mis. `motorcar`, `motorcycle`) tidak disertakan dalam file ini.

Properti tambahan juga disertakan, seperti `surface` (jenis permukaan jalan, misal `paving_stones`) dan data akses kendaraan (`motorcar`, `motorcycle`, dll.).

## 💻 Penggunaan

File `map.geojson` ini dapat langsung digunakan untuk visualisasi data atau analisis geospasial. Anda dapat memuatnya menggunakan:

* Layanan online seperti **geojson.io** untuk visualisasi dan pengecekan cepat.
* *Library* pemetaan web (**Google Maps API**).
