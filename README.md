## memory leaks
### Deskripsi:
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
