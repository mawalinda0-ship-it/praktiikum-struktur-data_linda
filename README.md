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
