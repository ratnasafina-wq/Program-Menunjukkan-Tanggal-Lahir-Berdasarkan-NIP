# Program-Menunjukkan-Tanggal-Lahir-Berdasarkan-NIP
Program ini akan menunjukkan tanggal lahir seorang ASN berdasarkan 8 digit awal NIP diikuti dengan 10 digit NIP. Di mana, 4 digit pertama menunjukkan tahun kelahiran, 2 digit berikutnya menunjukkan bulan kelahiran, dan 2 digit berikutnya menunjukkan tanggal kelahiran.

nip = input("Masukkan NIP (18 digit): ")
print("NIP: ", nip)

if len(nip) != 18 :
  print("Tanggal Lahir: NIP tidak valid! (NIP harus tepat 18 digit)")
else :
  tgl_lahir = nip[0:8]

  tahun = tgl_lahir[0:4]
  bulan = int(tgl_lahir[4:6])
  tanggal = int(tgl_lahir[6:8])

if bulan == 1 :
  nama_bulan = "Januari"
  maks_tanggal = 31
elif bulan == 2 :
  nama_bulan = "Februari"
  maks_tanggal = 29
elif bulan == 3 :
  nama_bulan = "Maret"
  maks_tanggal = 31
elif bulan == 4 :
  nama_bulan = "April"
  maks_tanggal = 30
elif bulan == 5 :
  nama_bulan = "Mei"
  maks_tanggal = 31
elif bulan == 6 :
  nama_bulan = "Juni"
  maks_tanggal = 30
elif bulan == 7 :
  nama_bulan = "Juli"
  maks_tanggal = 31
elif bulan == 8 :
  nama_bulan = "Agustus"
  maks_tanggal = 31
elif bulan == 9 :
  nama_bulan = "September"
  maks_tanggal = 30
elif bulan == 10 :
  nama_bulan = "Oktober"
  maks_tanggal = 31
elif bulan == 11 :
  nama_bulan = "November"
  maks_tanggal = 30
elif bulan == 12 :
  nama_bulan = "Desember"
  maks_tanggal = 31
else :
  nama_bulan = "Kode bulan pada NIP tidak valid!"
  maks_tanggal = None

if pd.isna(maks_tanggal) :
  print("Tanggal Lahir: ", nama_bulan)
elif tanggal < 1 or tanggal > maks_tanggal :
  print("Tanggal Lahir: Kode tanggal pada NIP tidak valid!")
else :
  print("Tanggal Lahir: ", tanggal, nama_bulan, tahun)
