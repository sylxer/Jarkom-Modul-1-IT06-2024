# Laporan-Resmi-Jarkom-Modul-1-IT06-2024

| Nama                      | NRP                       |
|---------------------------|---------------------------|
| Muhammad Harvian Dito S.  | 5027221039                |
| Sylvia Febrianti          | 5027221019                |


## Fuzz

1. Dilakukan filter string terhadap POST yang dilakukan oleh attacker. Didapatkan informasi IP yang digunakan yaitu 10.33.1.154. Attacker menggunakan port web server 80 dan endpoint '/'.

![Screenshot 2024-04-03 134041](https://github.com/sylxer/Jarkom-Modul-1-IT06-2024/assets/115382618/648b1b2d-97b8-4ae7-ac45-e8a5dea44c9c)

2. Dilakukan filter tcp.stream eq 1. Kemudian pada didalamnya terdapat informasi mengenai tools yang digunakan serta versinya dan juga email dan password yang berhasil digunakan attacker untuk login (ditandai dengan return 302 found).

![Screenshot 2024-04-03 134348](https://github.com/sylxer/Jarkom-Modul-1-IT06-2024/assets/115382618/88424a8b-118f-4209-882a-c63532b005f6)

3. Jawab seluruh pertanyaan yang terdapat pada netcat.

![fuzz](https://github.com/sylxer/Jarkom-Modul-1-IT06-2024/assets/115382618/73250327-ebbf-42d9-bdf8-0edcf4075d11)

## Whoami

1. Pada filter tcp.stream eq 7 terdapat sebuah build code C yang memiliki comment mencurigakan.

![Screenshot 2024-04-03 134706](https://github.com/sylxer/Jarkom-Modul-1-IT06-2024/assets/115382618/4ab85437-d021-4804-a298-e0d8acf58499)

2. Ketika di-decode menggunakan base64 menghasilkan pesan output sebagai berikut.

![Screenshot 2024-04-03 134747](https://github.com/sylxer/Jarkom-Modul-1-IT06-2024/assets/115382618/205babc8-163e-48bd-a495-07e6a6854f82)

3. Jawab pertanyaan pada netcat.

![whoami](https://github.com/sylxer/Jarkom-Modul-1-IT06-2024/assets/115382618/db29e5a3-6397-40bf-8174-24776c4fbcdd)

## ATM or ATP or FTP?

1. Pada stream terakhir terdapat login successful. Dapat dicari dengan menggunakan string 'success' search dalam packet details.

![Screenshot 2024-04-03 134946](https://github.com/sylxer/Jarkom-Modul-1-IT06-2024/assets/115382618/4cde0b40-cb0c-405f-8f5c-5dbca89c40c7)

2. Jawab pertanyaan pada netcat.

![atm](https://github.com/sylxer/Jarkom-Modul-1-IT06-2024/assets/115382618/629acb4a-e6b2-4756-8d0c-f88ec60c18c1)

## Trace Him

1. Pada tcp.stream eq 319, terdapat percobaan request dari suatu IP yang menunjukkan IP attacker (ditandai dengan request yang dilakukan oleh attacker).

![Screenshot 2024-04-03 135120](https://github.com/sylxer/Jarkom-Modul-1-IT06-2024/assets/115382618/d9fc0b8c-d9d0-41a0-a447-f369b0dceb11)

2. Jawab pertanyaan pada netcat.

![trace him](https://github.com/sylxer/Jarkom-Modul-1-IT06-2024/assets/115382618/4b84f36f-8ccf-4682-8a33-4dc8c8fd31ac)

## Evidence

1. Mencari POST. Kemudian dilakukan follow TCP stream-nya. Didapatkan domain, versi web server, dan endpoint.

![Screenshot 2024-04-03 141407](https://github.com/sylxer/Jarkom-Modul-1-IT06-2024/assets/115382618/2f5ed8a9-75cd-418a-a115-1d34c15efafd)

2. Kemudian mencari email dan password dengan mencari string 'success' pada packet details. Didapatkan email dan password yang berhasil login dengan return Login Successful.

![Screenshot 2024-04-03 141520](https://github.com/sylxer/Jarkom-Modul-1-IT06-2024/assets/115382618/13b650b0-84fd-450e-a299-d94c6d40a274)

3. Jawab pertanyaan pada netcat.

![evidence](https://github.com/sylxer/Jarkom-Modul-1-IT06-2024/assets/115382618/8ba85db8-a860-4a05-a783-85019d934938)
