## Off-by-One Errors
### Deskripsi:
Off-by-one error adalah kesalahan logika yang terjadi ketika loop atau kondisi tidak menangani batas dengan benar, sering kali menyebabkan iterasi yang salah atau akses memori yang tidak valid.
```c

```


## memory leaks
#### Deskripsi:
Memory leak terjadi ketika program mengalokasikan memori tetapi tidak membebaskannya setelah selesai digunakan. Ini dapat menyebabkan penggunaan memori yang berlebihan dan akhirnya mengakibatkan program kehabisan memori.
### Contoh:
```c
#include <stdlib.h>

void memory_leak() {
    int* arr = (int*)malloc(10 * sizeof(int)); // Alokasikan memori
    // Tidak ada free(arr); di sini
}

int main() {
    memory_leak();
    return 0; // Memori yang dialokasikan tidak dibebaskan
}

```
## Buffer Overflow
### Deskripsi:
Buffer overflow terjadi ketika program menulis lebih banyak data ke buffer (array) daripada yang dapat ditampung. Ini dapat menyebabkan kerusakan data, crash program, atau kerentanan keamanan.
### Contoh:
```c
#include <stdio.h>
#include <string.h>

int main() {
    char buffer[10];
    strcpy(buffer, "This is a long string"); // Menyalin string yang lebih panjang dari buffer
    printf("%s\n", buffer);
    return 0;
}

```


## Segmentation Fault
### Deskripsi:
Segmentation fault terjadi ketika program mencoba mengakses memori yang tidak diizinkan, seperti dereferencing pointer yang tidak valid atau mengakses memori di luar batas array.
### Contoh:
```c
#include <stdio.h>

int main() {
    int* ptr = NULL;
    *ptr = 10; // Mencoba dereference pointer NULL
    return 0;
}

```
