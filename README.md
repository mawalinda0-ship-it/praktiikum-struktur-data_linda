class Stack:
    def _init_(self):
        # Membuat list kosong untuk menyimpan elemen stack
        self.items = []

    def push(self, item):
        # Menambahkan item ke tumpukan (di akhir list)
        self.items.append(item)

    def pop(self):
        # Menghapus dan mengembalikan elemen terakhir (top of stack)
        if not self.is_empty():
            return self.items.pop()
        return None

    def peek(self):
        # Melihat elemen di atas stack tanpa menghapusnya
        if not self.is_empty():
            return self.items[-1]
        return None

    def is_empty(self):
        # Mengecek apakah stack kosong
        return len(self.items) == 0

    def size(self):
        # Mengembalikan jumlah elemen dalam stack
        return len(self.items)

        class Queue:
    def __init__(self):
        # Menggunakan deque agar operasi efisien di kedua ujung
        self.items = deque()

    def enqueue(self, item):
        # Menambahkan item ke belakang antrian
        self.items.append(item)

    def dequeue(self):
        # Menghapus dan mengembalikan item dari depan antrian
        if not self.is_empty():
            return self.items.popleft()
        return None

    def front(self):
        # Melihat elemen pertama dalam antrian tanpa menghapusnya
        if not self.is_empty():
            return self.items[0]
        return None

    def rear(self):
        # Melihat elemen terakhir dalam antrian tanpa menghapusnya
        if not self.is_empty():
            return self.items[-1]
        return None

    def is_empty(self):
        # Mengecek apakah antrian kosong
        return len(self.items) == 0

    def size(self):
        # Mengembalikan jumlah elemen dalam antrian
        return len(self.items)


    
PENJELASAN 
1. class Stack:
Mendefinisikan sebuah kelas bernama Stack. Kelas ini digunakan untuk membuat struktur data tumpukan (stack).
2. def _init_(self):
Ini seharusnya adalah __init__, yaitu konstruktor yang akan dijalankan saat objek dibuat.
Karena kamu menulis _init_, maka konstruktor tidak akan dijalankan.
Seharusnya:
def __init__(self):
3. self.items = []
Membuat atribut bernama items yang berbentuk list kosong.
List ini digunakan untuk menyimpan elemen-elemen dalam stack.
4. def push(self, item):
Membuat fungsi push yang digunakan untuk menambahkan elemen ke dalam stack.
5. self.items.append(item)
Menambahkan item ke akhir list, yang merupakan posisi paling atas (top) pada stack.
6. def pop(self):
Membuat fungsi pop yang digunakan untuk menghapus dan mengambil elemen paling atas dari stack.
7. if not self.is_empty():
Memeriksa apakah stack tidak kosong sebelum melakukan pop.
Ini mencegah error ketika menghapus elemen dari stack yang kosong.
8. return self.items.pop()
Jika stack tidak kosong, ambil dan hapus elemen terakhir (top of stack), lalu kembalikan nilainya.
9. return None
Jika stack kosong, fungsi pop() mengembalikan None sebagai tanda tidak ada elemen yang diambil.
10. def peek(self)
Membuat fungsi peek, untuk melihat elemen paling atas tanpa menghapusnya.
11. if not self.is_empty():
Memeriksa apakah stack tidak kosong.
12. return self.items[-1]
Mengambil elemen paling atas (index -1) namun tidak menghapusnya.
13. return None
Jika stack kosong, mengembalikan None.
14. def is_empty(self):
Membuat fungsi untuk mengecek apakah stack kosong atau tidak.
15. return len(self.items) == 0
Jika panjang list = 0, berarti stack kosong → mengembalikan True.
16. def size(self):
Membuat fungsi size untuk mengetahui jumlah elemen di dalam stack.
17. return len(self.items)
Mengembalikan jumlah elemen dalam stack (bukan boolean).






