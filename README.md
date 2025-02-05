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

```
