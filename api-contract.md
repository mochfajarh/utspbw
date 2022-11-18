## Mahasiswa
<details>
<summary> Klik untuk Ekspan </summary>

### Create Mahasiswa
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/mahasiswa </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> POST </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Body</b> </td>
<td>

``` json
{
    "nama" : "Fajar",
    "alamat" : "Cibedug",
    "hobi" : "Hiking dan Olahraga"
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 201,
    "message" : "Data Mahasiswa Berhasil diinput",
    "data" : {
        "id" : 1234,
        "nama" : "Fajar",
        "alamat" : "Cibedug",
        "hobi" : "Hiking dan Olahraga"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Conflict</b> </td>
<td>

``` json
{
    "code" : 409,
    "message" : "Nama Mahasiswa Telah digunakan",
    "data" : {
        "value" : "Fajar",
        "property" : "nama",
        "location" : "body"
    } 
}    
```

</td>
</tr>
</table>


### Read Mahasiswa By Id
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/mahasiswa </td>
</tr>
<tr>
    <td> <b>Example</b> </td>
    <td> {{baseURL}}/api/v1/mahasiswa?id=1234 </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> GET </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Query</b> </td>
<td> id=1234 </td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 200,
    "message" : "Sukses",
    "data" : {
        "id" : 1234,
        "nama" : "Fajar",
        "alamat" : "Cibedug",
        "hobi" : "Hiking dan Olahraga"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Not Found</b> </td>
<td>

``` json
{
    "code" : 404,
    "message" : "ID Mahasiswa tidak ditemukan",
    "data" : {
        "value" : 1234,
        "property" : "id",
        "location" : "query"
    } 
}    
```

</td>
</tr>
</table>


### Read Mahasiswa All
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/mahasiswa </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> GET </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 200,
    "message" : "Sukses",
    "data" : [
        {
            "id" : 1234,
            "nama" : "Fajar",
            "alamat" : "Cibedug",
            "hobi" : "Hiking dan Olahraga"
        },
        {
            "id" : 1235,
            "nama" : "Risfan",
            "alamat" : "Cigombong",
            "hobi" : "Sepak Bola"
        }
    ]
}    
```

</td>
</tr>
</table>

### Update Mahasiswa
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/mahasiswa </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> PUT </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Body</b> </td>
<td>

``` json
{
    "id" : 1234,
    "nama" : "Moch Fajar Hikmatulloh",
    "alamat" : "Cibedug-Tapos",
    "hobi" : "Hiking dan Olahraga"
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 201,
    "message" : "Data Mahasiswa Berhasil diubah",
    "data" : {
        "id" : 1234,
        "nama" : "Moch Fajar Hikmatulloh",
        "alamat" : "Cibedug-Tapos",
        "hobi" : "Hiking dan Olahraga"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Conflict</b> </td>
<td>

``` json
{
    "code" : 409,
    "message" : "Nama Mahasiswa Telah digunakan",
    "data" : {
        "value" : "Moch Fajar Hikmatulloh",
        "property" : "nama",
        "location" : "body"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Not Found</b> </td>
<td>

``` json
{
    "code" : 404,
    "message" : "ID Mahasiswa tidak ditemukan",
    "data" : {
        "value" : 1234,
        "property" : "id",
        "location" : "body"
    } 
}    
```

</td>
</tr>
</table>

### Delete Mahasiswa
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/mahasiswa </td>
</tr>
<tr>
    <td> <b>Example</b> </td>
    <td> {{baseURL}}/api/v1/mahasiswa?id=1234 </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> DELETE </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Query</b> </td>
<td> id=1234 </td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 200,
    "message" : "Sukses dihapus",
    "data" : [] 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Not Found</b> </td>
<td>

``` json
{
    "code" : 404,
    "message" : "ID Mahasiswa tidak ditemukan",
    "data" : {
        "value" : 1234,
        "property" : "id",
        "location" : "query"
    } 
}    
```

</td>
</tr>
</table>
</details>

## Dosen
<details>
<summary> Klik untuk Ekspan </summary>

### Create Dosen
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/dosen </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> POST </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Body</b> </td>
<td>

``` json
{
    "nama" : "MA’SHUM ABDUL JABBAR, S.KOM, M.T.I.",
    "alamat" : "Jakarta Timur",
    "hobi" : "Tidak Tahu hehe"
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 201,
    "message" : "Data Dosen Berhasil diinput",
    "data" : {
        "id" : 1234,
        "nama" : "MA’SHUM ABDUL JABBAR, S.KOM, M.T.I.",
        "alamat" : "Jakarta Timur",
        "hobi" : "Tidak Tahu hehe"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Conflict</b> </td>
<td>

``` json
{
    "code" : 409,
    "message" : "Nama Dosen Telah digunakan",
    "data" : {
        "value" : "MA’SHUM ABDUL JABBAR, S.KOM, M.T.I.",
        "property" : "nama",
        "location" : "body"
    } 
}    
```

</td>
</tr>
</table>


### Read Dosen By Id
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/dosen </td>
</tr>
<tr>
    <td> <b>Example</b> </td>
    <td> {{baseURL}}/api/v1/dosen?id=1234 </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> GET </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Query</b> </td>
<td> id=1234 </td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 200,
    "message" : "Sukses",
    "data" : {
        "id" : 1234,
        "nama" : "MA’SHUM ABDUL JABBAR, S.KOM, M.T.I.",
        "alamat" : "Jakarta Timur",
        "hobi" : "Tidak Tahu hehe"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Not Found</b> </td>
<td>

``` json
{
    "code" : 404,
    "message" : "ID Dosen tidak ditemukan",
    "data" : {
        "value" : 1234,
        "property" : "id",
        "location" : "query"
    } 
}    
```

</td>
</tr>
</table>


### Read Dosen All
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/dosen </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> GET </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 200,
    "message" : "Sukses",
    "data" : [
        {
            "id" : 1234,
            "nama" : "MA’SHUM ABDUL JABBAR, S.KOM, M.T.I.",
            "alamat" : "Jakarta Timur",
            "hobi" : "Tidak Tahu hehe"
        },
        {
            "id" : 1235,
            "nama" : "Mulil Khaira, S.Kom., M.Kom.",
            "alamat" : "Sekarang di Bogor",
            "hobi" : "Tidak Tahu hehe"
        }
    ]
}    
```

</td>
</tr>
</table>

### Update Dosen
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/dosen </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> PUT </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Body</b> </td>
<td>

``` json
{
    "id" : 1234,
    "nama" : "TMA’SHUM ABDUL JABBAR, S.KOM, M.T.I.",
    "alamat" : "Jakarta Timur",
    "hobi" : "Tidak Tahu hehe"
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 201,
    "message" : "Data Dosen Berhasil diubah",
    "data" : {
        "id" : 1234,
        "nama" : "MA’SHUM ABDUL JABBAR, S.KOM, M.T.I.",
        "alamat" : "Jakarta Timur",
        "hobi" : "Tidak Tahu hehe"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Conflict</b> </td>
<td>

``` json
{
    "code" : 409,
    "message" : "Nama Dosen Telah digunakan",
    "data" : {
        "value" : "MA’SHUM ABDUL JABBAR, S.KOM, M.T.I.",
        "property" : "nama",
        "location" : "body"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Not Found</b> </td>
<td>

``` json
{
    "code" : 404,
    "message" : "ID Dosen tidak ditemukan",
    "data" : {
        "value" : 1234,
        "property" : "id",
        "location" : "body"
    } 
}    
```

</td>
</tr>
</table>

### Delete Dosen
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/dosen </td>
</tr>
<tr>
    <td> <b>Example</b> </td>
    <td> {{baseURL}}/api/v1/dosen?id=1234 </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> DELETE </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Query</b> </td>
<td> id=1234 </td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 200,
    "message" : "Sukses dihapus",
    "data" : [] 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Not Found</b> </td>
<td>

``` json
{
    "code" : 404,
    "message" : "ID Dosen tidak ditemukan",
    "data" : {
        "value" : 1234,
        "property" : "id",
        "location" : "query"
    } 
}    
```

</td>
</tr>
</table>
</details>