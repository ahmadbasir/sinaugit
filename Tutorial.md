
# Tutorial Git __Dasar__ :: madeInDewe

### Instalasi Git

```
	$ git init
```
> <span style="color:red">git init</span> adalah perintah untuk **_menginisialisasi_** direktori atau folder
> misalkan kita mempunyai folder bernama **_project_** kemudian ingin menginisialisasi
> git kedalamnya maka kita perlu masuk dulu ke dalam foldernya
```
	$ cd project
	$ git init
```
dengan begitu kita sudah menginisialisasi folder **_project_** untuk menggunakan **_.git_**



### Mendownload Project ke Local

```
	$ git clone %url
```
> __*git clone*__, seperti nama nya berfungsi untuk mengclone sebuah project ke local
> atau bahasa awamnya mendownlaod repositori / project keLocal

example :
```
	$ git clone https://github.com/ahmadbasir/sinaugit.git
```

### Cek-Updated file
```
	$ git status
```
> ketika kita melakukan perubahan pada sebuah file, atau ingin mengetahui fila apasaja yang telah kita rubah, maka __$ git status__ adalah perintah untuk melakukannya

misalkan kita memiliki file __.ubah1__ dengan isi sebagai berikut :
```
! ini isi 1
```
kemudia kalian merubah menjadi :
```
! menjadi isi 2
```
jika kalian melakukan ```$ git status``` maka akan muncul informasi ```modified : .ubah1``` dengan tulisan warna merah

### Penambahan Tracked-File

```
	$ git add %name_file
```
> berfungsi untuk memnambahkan file untuk __dipantau__, misalkan kita memiliki file __.gaje__ dalam keadaan default file tersebut sudah terpantau, namun jika kita memnambahkan file baru misalkan __.gaje2__ untuk bisa melihat perubahan pada __.gaje2__ kita perlu manmbahkan daftar pantau dengan comment

```
	$ git add .gaje2
```
maka file __.gaje2__ akan automatis terTrack jika ada perubahan

> menyangkut dari perintah ``` $ git status``` yang tulisan **```modified : %file-name```** seletah di ```$ git add ..``` maka tulisan akan berubah menjadi hijau yang artinya file tersebut sudah ditambahkan.


### Commit message .updating repositori
```
	$ git commit -m 'ini pesan'
```
> ```$ git commit``` merupakan perintah untuk mengirim notifikasi sekaligus memferifikasi apa yang berubah pada repositori

__perlu dicatat__ setiap perubahan pada repositori yang ingin di __push__ harus melakukan ```git commit``` terlbih dahulu. karena git commit disini memberitahukan apa saja yang telah berubah. jadi ketika kita sedang mengerjakan sebuah proyek bersama kita tahu dimana kita mengubah file ataupun membuat direktori baru.


### Branching 'Pencabangan'
```
	$ git branch
	$ git branch %new-branch
	$ git branch -d %deleted-branch
```
> setiap repository pasti memiliki cabang, dimana cabang utama adalah **```master```** bracnh, master branch adalah cabang utama ketika membuat sebuah repositori baru ```by default```

untuk mengecek kita sedang berada dibranch mana bisa diketikan perintah
```
	$ git status
```
maka akan muncul status branch saat ini. dan untuk melakukan pengecekan branch yang telah kita buat bisa dengan perintah **```$ git branch```** kemudian untuk penambahan branch baru kita cukup menambahkan nama branch setelah command __branch__ misalnya kita ingin menambahkan branch dengan nama __nganu__ cukup ketikan perintah

```
	$ git branch nganu
```
> voila! kita telah menambah kan branch baru dengan nama **```nganu```**, bisa dicek dengan perintah ```$ git branch```

untuk menghapus bracnh, kita cukup menambahkan **```-b```** diikuti dengan ```nama-branch``` yang ingin dihapus setelah ```$ git branch``` misal kita ingin menghapus bracnh ```editer``` maka tulisan perintah seperti berikut :

```
	$ git branch -d editer <-- ini nama branch
```


### Perpindahan Branch
```
	$ git checkout %nama-branch
```
> seandainya kita memiliki 2 buah branch yaitu ```master``` dan ```editer``` posisi branch default kita itu terletak pada branch master, jika kita ingin mengubah atau pindah ke branch ```editer``` kita bisa menggunakan perintah tersebut

```
	$ git checkout editer
```
Maka kita sudah berpindah pada branch ```editor``` ada beberapa rule dalam penggunaan branch. membahas point sebelumnya __```Branching```___ digunakan untuk memanage tugas/project agar terstruktur, biasanya dalam melakukan project dilakukan banyak Pencabangan / ```Branching``` hal ini bertujuan agar tidak ```saling tumbuk	```

> ada beberapa perintah unik dalam ```$ git checkout``` yaitu melakukan perpindahan branch sekaligus menambah branch baru. berikut command line nya

```
	$ git checkout -b %new-branch
```
misalkan repositori telah memiliki 2 buah bracnh, yaitu :
>branch

* master
* editer

dan kita ingin menambahkan branch baru, kita tidak perlu melakukan proses dua kali dengan ```$ git bracnh %new-branch``` kemudian ```$ git checkout %name-branch``` melainkan dengan melakukan perintah berikut :

```
	$ git checkout -b contributor
```
disini kita telah membuat bracnh baru dengan nama ```contributor``` dan automatis checkout ke branch tersebut, bisa di cek dengan melakukan perintah **```$ git branch```**

> branch

* master
* editer
* contributor <-- ini adalah branch baru

kemudian coba melakukan perintah ```$ git status```
>status on branch
>* contributor <br>
>noting to commit bla bloa bla...

###
