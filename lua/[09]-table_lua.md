## Table
*Table* pada __lua__ sama seperti *Array*, *List*, ataupun *Object* di bahasa pemrograman lain. *Table* dapat diisi tipe data yang berbeda - beda.
Contoh *Table* adalah `local tbl = {"This", 2, 9.9, true, {"ok","cool"}}`.
Jika kita melakukan `print(tbl)` maka yang akan muncul adalah *memory address*.
Untuk mengakses variabel di dalam *table* dapat menggunakan
```lua
for i = 1, #tbl do
    print(tbl[i])
end
-- semua variabel akan ditampilkan

```
di __lua__ *index* dimulai dari 1 (sigh!). Sehingga kita dapat mengakses variabel pertama pada *table* menggunakan `print(tbl[1])` maka akan mencetak item pertama.

## Manipulasi Table
Insert
```lua
local nums = {1, 3, 5, 7, 9}
table.insert(nums, 19) -- 19 akan ditambahkan setelah angka 9
table.insert(nums, 2, 20) -- 20 akan ditambahkan di index ke-2
table.remove(nums, 2) -- Variabel di index ke-2 akan dihapus
for i, #nums do
    print(nums[i])
end
--mengubah isi value table ke dalam string
print(table.concat(nums," ")) -- outputnya 1 3 5 7 9
```

## Alternatif Mengakses Value di Dalam Table
```lua
local nums = {1, 3, 5, 7, 9}
for index, value in pairs(nums) do
    print(index, value)
end
-- akan mencetak index, dan value di index tersebut
```

## Multidimensional Table
```lua
local nums = {
    {1, 8, 3}, -- index 1
    {4, 2, 6}, -- index 2
    {7, 5, 9}, -- index 3
    }
print(nums[1][2]) -- outputnya 8
```
Untuk mengakses seluruh value dalam *Multidimensional Table*, gunakan
```lua
for i = 1, #nums do
    for j = 1, #nums[i] do
        print(nums[i][j])
    end
end
```

## Named Table
```lua
local tbl = {
        name = "Mike",
        age = 12
}
print(tbl["name"]) -- outputnya Mike
```
