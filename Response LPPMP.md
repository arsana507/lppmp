# Response LPPMP

1. __Login__
2. __Cookie Login__
3. __Autocomplete Dosen__
4. __Get Nama Dosen__
5. __Get All Prodi__
6. __Get Nama Prodi__
7. __Get All Fakultas__
8. __Get Nama Fakultas__
9. __Get Tahun Akademik Aktif__

#
# LOGIN
### Login sebagai dosen
##   -

__METHOD__
```
POST
```

__Sample Request__
```
{
    "username": "0021807008",
    "password": "Ubharaj4y4"
}
```


### -
### Jika Lecturer
### -

__Sample Response__
```
{
    "status": 1,
    "message": "success",
    "data": {
        "username": "0021807008",
        "usertype": "1",
        "userid": "0021807008",
        "nidn": "0321127201",
        "group": "7,6",
        "name": "R. Wisnu Prio Pamungkas, S.Kom., M.Kom",
        "nik": null,
        "tplhr": "Jakarta",
        "tglhr": "0000-00-00",
        "jenkel": "P",
        "hp": "0818912153",
        "jabfung": "SAH",
        "email": "rwisnup.pamungkas@gmail.com",
        "fakultas": "2",
        "prodi": "55201"
    }
}
```

### -
### Jika Administrator
### -

__Sample Response__
```
{
    "status": 1,
    "message": "success",
    "data": {
        "username": "LPPMP",
        "usertype": "6",
        "userid": "LPPMP",
        "group": "25",
        "name": "Lembaga Penelitian dan Pengabdian Masyarakat",
        "nik": "",
        "tplhr": "",
        "tglhr": "",
        "jenkel": "",
        "hp": "",
        "email": ""
    }
}
```

#
# COOKIE LOGIN
### Login sebagai dosen
##   -

__METHOD__
```
POST
```

__Sample Request__
```
{
    "username": "0021807008",
    "usertype": "1"
}
```


### -
### Jika Lecturer
### -

__Sample Response__
```
{
    "status": 1,
    "message": "success",
    "data": {
        "username": "0021807008",
        "usertype": "1",
        "userid": "0021807008",
        "nidn": "0321127201",
        "group": "7,6",
        "name": "R. Wisnu Prio Pamungkas, S.Kom., M.Kom",
        "nik": null,
        "tplhr": "Jakarta",
        "tglhr": "0000-00-00",
        "jenkel": "P",
        "hp": "0818912153",
        "jabfung": "SAH",
        "email": "rwisnup.pamungkas@gmail.com",
        "fakultas": "2",
        "prodi": "55201"
    }
}
```

### -
### Jika Administrator
### -

__Sample Response__
```
{
    "status": 1,
    "message": "success",
    "data": {
        "username": "LPPMP",
        "usertype": "6",
        "userid": "LPPMP",
        "group": "25",
        "name": "Lembaga Penelitian dan Pengabdian Masyarakat",
        "nik": "",
        "tplhr": "",
        "tglhr": "",
        "jenkel": "",
        "hp": "",
        "email": ""
    }
}
```

#
## AUTOCOMPLETE DOSEN
#

### Autocomplete dosen dengan memasukkan beberapa karakter dari NID ataupun NAMA DOSEN
### -

__METHOD__
```
POST
``` 

__Sample Request__
```
{
    "term": "wis"
}
```

__Sample Response__
```
{
    "status": 1,
    "message": "success",
    "data": [
        {
            "label": "010803018 - M. Hanafi Darwis, Dr. Ir, SH, MM",
            "value": "010803018 - M. Hanafi Darwis, Dr. Ir, SH, MM",
            "save": "010803018",
            "name": "M. Hanafi Darwis, Dr. Ir, SH, MM",
            "nidn": "0323015604",
            "telp": "08121801402",
            "email": "hanafidarwis@gmail.com",
            "fakultas": "3",
            "fakultasname": "HUKUM",
            "jabfung": "LKT",
            "jabfungname": "Lektor"
        },
        {
            "label": "0021807008 - R. Wisnu Prio Pamungkas, S.Kom., M.Kom",
            "value": "0021807008 - R. Wisnu Prio Pamungkas, S.Kom., M.Kom",
            "save": "0021807008",
            "name": "R. Wisnu Prio Pamungkas, S.Kom., M.Kom",
            "nidn": "0321127201",
            "telp": "0818912153",
            "email": "rwisnup.pamungkas@gmail.com",
            "fakultas": "2",
            "fakultasname": "TEKNIK",
            "jabfung": "SAH",
            "jabfungname": "Asisten Ahli"
        }
    ]
}
```

#
## GET NAMA DOSEN
#
### Get nama dosen berdasarkan NID
### -
__METHOD__
```
POST
```

__Sample Request__
```
{
    "nid": "0021807008"
}
```

__Sample Response__
```
{
    "status": 1,
    "message": "success",
    "data": "R. Wisnu Prio Pamungkas, S.Kom., M.Kom"
}
```

#
## GET ALL PRODI
#
### Get semua prodi
### -

__METHOD__
```
GET
```

__Sample Response__
```
{
    "status": 1,
    "message": "success",
    "data": [
        {
            "id_prodi": "5",
            "kd_prodi": "62201",
            "prodi": "AKUNTANSI",
            "kd_fakultas": "1",
            "jenjang": "S1",
            "id_sms": "a26699d1-68f5-43cd-9eea-183d02932b8a",
            "sk": "217/SK/BAN-PT/Ak-XVI/S/X/2013",
            "akreditasi": "C",
            "tahun_akreditasi": "2013",
            "tgl_kadaluarsa": "2018-10-26",
            "status_prodi": "1",
            "kaprodi": "031703067",
            "prodi_en": null
        },
        {
            "id_prodi": "7",
            "kd_prodi": "73201",
            "prodi": "PSIKOLOGI",
            "kd_fakultas": "5",
            "jenjang": "S1",
            "id_sms": "683afb04-010d-4a79-bb9e-cae295051ebb",
            "sk": "1104/SK/BAN-PT/Akred/S/IV/2017",
            "akreditasi": "C",
            "tahun_akreditasi": "2017",
            "tgl_kadaluarsa": "2022-04-18",
            "status_prodi": "1",
            "kaprodi": "051512039",
            "prodi_en": null
        }
    ]
}
```

#
## GET PRODI NAME
#
### Get nama prodi berdasarkan kode prodi
### -

__METHOD__
```
POST
```

__Sample Request__
```
{
    "kd_prodi": "62201"
}
```

__Sample Response__
```
{
    "status": 1,
    "message": "success",
    "data": "AKUNTANSI"
}
```

#
## GET ALL FAKULTAS
#
### Get semua fakultas
### -

__METHOD__
```
GET
```

__Sample Response__
```
{
    "status": 1,
    "message": "success",
    "data": [
        {
            "id_fakultas": "5",
            "kd_fakultas": "1",
            "fakultas": "EKONOMI",
            "dekan": "031905085"
        },
        {
            "id_fakultas": "1",
            "kd_fakultas": "2",
            "fakultas": "TEKNIK",
            "dekan": "029609002"
        }
    ]
}
```


#
## GET FAKULTAS NAME
#
### Get nama fakultas berdasarkan kode fakultas
### -

__METHOD__
```
POST
```

__Sample Request__
```
{
    "kd_fakultas" : "2"
}
```

__Sample Response__
```
{
    "status": 1,
    "message": "success",
    "data": "EKONOMI"
}
```


#
## GET ACTIVE YEAR
#
### Get tahun akademik yang sedang aktif
### -

__METHOD__
```
GET
```

__Sample Response__
```
{
    "status": 1,
    "message": "success",
    "data": {
        "nama_tahun": "2020 / Ganjil",
        "kode_tahun": "20201"
    }
}
```