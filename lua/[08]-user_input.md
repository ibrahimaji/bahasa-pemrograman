## User Input
*User Input* digunakan untuk mendapatkan masukan dari pengguna.
```lua
print("Siapa nama Anda?")
local nama = io.read()
print("Nama Anda adalah" .. nama)
```
Untuk membuat kursor pengisian sejajar dengan *string* pertanyaan, dapat menggunakan
```lua
io.write("Masukkan nama Anda: ")
local nama = io.read()
print("Nama Anda adalah " .. nama)
```
