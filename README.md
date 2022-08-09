# UAS-ALGORITMA-1214012-JASMINE-MUTIARA-BINTANG-D4TI1A
   Nama                     : Jasmine Mutiara Bintang 
Kelas                      : 1A/ D4 Teknik Informatika 
NPM                      : 1214012 
Dosen Pengampu : Mohamad Nurkamal Fauzan 

Kode Program:
   public void act()
    {
        // Add your action code here.
        keycontrol();
    }
   public void keycontrol()
    {
    if(Greenfoot.isKeyDown("d"))
        {
            move(5);
        }
        
        if(Greenfoot.isKeyDown("a"))
        {
            move(-5);
        }
        
        if(Greenfoot.isKeyDown("s"))
        {
            setLocation(getX(),getY()+5);
        }
        
        if(Greenfoot.isKeyDown("w"))
        {
            setLocation(getX(),getY()-5);
        }
    }
}

Penjelasannya : 
    public void act()  
    {  
 	//Add your action code here keycontrol();  	 
    }  
 
Penjelasan:
Keycontrol sendiri yaitu untuk mengarahkan atau menjalankan actor bee (lebah) melalui keyboard panah (s, a, d, w) dimana kita harus mengetikkan kode melalui keyboard.
public void keycontrol()
    {
        if(Greenfoot.isKeyDown("d"))
        {
            move(5);
        }
        
        if(Greenfoot.isKeyDown("a"))
        {
            move(-5);
        }
        
        if(Greenfoot.isKeyDown("s"))
        {
            setLocation(getX(),getY()+5);
        }
        
        if(Greenfoot.isKeyDown("w"))
        {
            setLocation(getX(),getY()-5);
        }
    }
}

Penjelasan: 
Kode program diatas adalah sebuah kode program yang mana tujuannya adalah untuk mengarahkan sebuah keyboard kearah yang diperintahkan misalnya keatas, kebawah, kekanan, dan kekiri. Kemudian, setelah membuat perintah yakni key control, setelah itu di extends public void key control. Disini terdapat sebuah perintah keyboard dimana ketika kita mengetikkan sebuah huruf di keyboard maka otomatis lebah(bee) akan berpindah posisi (move) sebanyak -5 atau +5. Maksudnya adalah lebah akan berpindah posisi sebanyak 5 kali kekanan dan 5 kai kiri attau dapat diinisialisasikan yakni getY, maupun getX. Berikut ini adalah perintah yang digunakan:
Jika keyboard diketikkan “d”  maka ia akan berpindah posisi ke kanan sebanyak 5 kali.
Jika keyboard diketikkan “a”  maka ia akan berpindah posisi ke kiri sebanyak -5 kali.
Jika keyboard diketikkan “s”  maka ia akan berpindah posisi ke bawah sebanyak 5 kali.
Jika keyboard diketikkan “w”  maka ia akan berpindah posisi ke atas sebanyak -5 kali.

Setelah membuat kode program untuk actor bee, selanjutnya membuat database terlebih dahulu. 
1.	Start Xampp
2.	Buka php my admin
3.	Kemudian buat nama database yaitu uas
4.	Buat nama tabel yaitu arah
5.	Klik primary key di kolom ID
6.	Buat kolom yang terdiri Dari id, dan kunci
Id disini adalah untuk nomor dari baris dimana dibuat INT karena berupa angka, kemudian kunci dimana dibuat VARCHAR karena berupa huruf. 
7.	Sesuaikan values nya untuk kolom id dan kunci yaitu 11
8.	Klik go

Untuk ID disi dengan angka nomor misalkan nomor 1, 2, 3 kemudian kolom Kunci disi dengan huruf w,a,s, atau d. 
Selanjutnya mengkoneksikannya ke database, caranya buat sebuah kelas pada database:
public class koneksi{
    private static Connection koneksi;
    public static Connection getKoneksi(){
        if(koneksi == null){
            try{
                String url="mysql://localhost:3306/uas";
                String user="root";
                String password="";
                DriverManager.registerDriver(
                new com.mysql.jdbc.Driver());
                koneksi = DriverManager.getConnection(url,user,password);
                }catch (SQLException t){
                    System.out.println("ERROR MEMBUAT KONEKSI");
            }
        }
        return koneksi;
    }
}

