from os import system

nama_menu = []
hrg_menu = []
menu_yg_dibeli = []
jumlah_pembelian = []
total_pembelian = []
total = 0
totalsemua = 0


def home():
    system('cls')
    print("+=============================+")
    print("+      M E N U  U T A M A     +")
    print("+=============================+")
    print('|1. Admin                     |')
    print('|2. Kasir                     |')
    print('|3. Exit                      |')
    print("+=============================+")

    pilihan = input('Anda adalah: ')

    if pilihan == '1':
        login_admin()
    elif pilihan == '2':
        login_kasir()
    else:
        print('Program Exit')
        exit()


def login_admin():
    system('cls')
    print("+=============================+")
    print("|     HALAMAN LOGIN ADMIN     |")
    print("+=============================+")
    username = input('masukan username : ')
    password = input('masukan password : ')

    if username == 'admin' and password == 'adminpass':
        print('login berhasil...')
        input()
        ubah_data_rest()
    else:
        print('login gagal coba lagi..')
        login_admin()


def ubah_data_rest():
    system('cls')
    print("+=============================+")
    print("Ubah Daftar Menu".center(32))
    print("+=============================+")
    print('| 1. Menambah data menu       |')
    print('| 2. Menampilkan data menu    |')
    print('| 3. Mengganti data menu      |')
    print('| 4. Menghapus data menu      |')
    print('| 5. Exit                     |')
    print("+=============================+")

    pilihan = input('Masukkan pilihan : ')
    if pilihan == '1':
        input_menu_rest()
    elif pilihan == '2':
        show_menu_rest()
    elif pilihan == '3':
        edit_menu_rest()
    elif pilihan == '4':
        delete_menu_rest()
    elif pilihan == '5':
        home()
    else:
        print('program exit')
        exit()


def input_menu_rest():
    system('cls')
    print('+============================+')
    print('Tambah Menu Restaurant'.center(30))
    print('+============================+')

    nama = input(' Nama menu : ')
    nama_menu.append(nama)
    harga = input(' Harga     : ')
    hrg_menu.append(harga)

    print("Berhasil disimpan!")
    kembali = input('\nKembali Tekan [enter]')
    ubah_data_rest()


def show_menu_rest():
    system('cls')
    if len(nama_menu) <= 0:
        print("Data tidak ada")
    else:
        print('=' * 50)
        print('|Nama Menu \t\t |Harga \t\t |')
        print('=' * 50)
        for i in range(len(nama_menu)):
            print('|%s' % nama_menu[i] + '\t\t  %s' % hrg_menu[i])
        print('=' * 50)
    kembali = input('\nKembali Tekan [enter]')
    ubah_data_rest()


def edit_menu_rest():
    system('cls')
    print('=' * 49)
    print('|ID \t |Nama Menu \t\t |Harga   \t|')
    print('=' * 49)
    for i in range(len(nama_menu)):
        print('|%d \t %s' % (i, nama_menu[i]) + '\t\t  %s' % hrg_menu[i])
    print('=' * 49)

    i = int(input('Inputkan Id Menu :'))
    if i >= len(nama_menu):
        print("No Tidak Ada")
        input()
        edit_menu_rest()
    else:
        nama_baru = input('\nNama Menu : ')
        nama_menu[i] = nama_baru

        harga_baru = input('Harga : ')
        hrg_menu[i] = harga_baru

    kembali = input('\nKembali Tekan [Enter]')
    ubah_data_rest()


def delete_menu_rest():
    system('cls')
    print('=' * 49)
    print('|ID \t |Nama Menu \t\t |Harga \t|')
    print('=' * 49)
    for i in range(len(nama_menu)):
        print('|%d \t  %s' % (i, nama_menu[i]) + '\t\t  %s' % hrg_menu[i])
    print('=' * 49)

    i = int(input('Inputkan Id Menu :'))
    if i >= len(nama_menu):
        print("Data Tidak Ada")
        input()
        delete_menu_rest()
    else:
        nama_menu.remove(nama_menu[i])
        hrg_menu.remove(hrg_menu[i])

    input('\nKembali Tekan [Enter]')
    ubah_data_rest()


def login_kasir():
    system('cls')
    print("+=============================+")
    print("|     HALAMAN LOGIN KASIR     |")
    print("+=============================+")
    print("Silahkan Login Terlebih dahulu")

    username = input("Masukkan Username : ")
    password = input("Masukkan Password : ")

    if username == "kasir" and password == "kasir":
        print("Login Telah Berhasil")
        menu_kasir()
    else:
        print("Username dan password yang dimasukkan salah")
        login_kasir()


def menu_kasir():
    system('cls')
    print('+============================+')
    print("Menu Kasir".center(30))
    print('+============================+')
    print("|1. Pemesanan                |")
    print("|2. Struk Pembelian          |")
    print("|3. Exit                     |")
    print('+============================+')

    pilihan = input("Masukkan pilihan : ")
    if pilihan == "1":
        pemesanan()
    elif pilihan == "2":
        struk()
    elif pilihan == "3":
        home()
    else:
        menu_kasir()


def pemesanan():
    global totalsemua
    global total
    global nama_menu

    system('cls')
    print("Daftar Menu".center(47))
    print('=' * 49)
    print('|N0 \t |Nama Menu \t\t |Harga \t|')
    print('=' * 49)
    for i in range(len(nama_menu)):
        print('|%d. \t  %s' % (i, nama_menu[i]) + '\t\t  %s' % hrg_menu[i])
    print('=' * 49)

    nama_pembeli = input("\nMasukkan Nama Pembeli : ")
    jml_beli = int(input("\nMasukkan Jumlah Transaksi : "))
    a = 0
    while a < jml_beli:
        i = int(input("\nMasukkan Pilihan Menu : "))
        if i <= len(nama_menu):
            print("Nama Menu : ", nama_menu[i])
            jumlah = int(input("Jumlah Pembelian : "))
            total = jumlah * int(hrg_menu[i])
            print(jumlah, nama_menu[i], ": Rp.", total)
            totalsemua = totalsemua + total
            jumlah_pembelian.append(str(jumlah))
            total_pembelian.append(str(totalsemua))
            menu_yg_dibeli.append(nama_menu[i])
        a += 1
    print("\nTotal bayar : Rp.", totalsemua)
    uang = int(input("Uang Tunai Pembeli: Rp. "))
    kembalian = int(uang - totalsemua)
    print("Kembalian : Rp.", kembalian)
    kembali = input('\nKembali Tekan [enter]')

    struk = open('struk.txt', 'w')
    struk.write("\n=====================================")
    struk.write("\n======== S T R U K   B E L I ========")
    struk.write("\n=====================================")
    struk.write("\n Nama         : " + nama_pembeli)
    struk.write('\n Beli         : ')
    for i in range(len(menu_yg_dibeli)):
        struk.write('%s' % str(jumlah_pembelian[i]) + '  %s' %
                    str(menu_yg_dibeli[i]) + '  Rp.%s' % str(total_pembelian[i] + '\n\t\t\t\t'))
    struk.write("\n Tagihan      : Rp." + str(totalsemua))
    struk.write("\n Uang         : Rp." + str(uang))
    struk.write("\n Kembalian    : Rp." + str(kembalian))
    struk.write("\n=====================================")
    struk.write("\n=====================================")
    struk.close()
    menu_kasir()


def struk():
    bacastruk = open("struk.txt", "r")
    print(bacastruk.read())

    kembali = input('\nKembali Tekan [enter]')
    menu_kasir()


home()
