# Reverse Engineering Practice Book

* **`Linux`**: Compile each program with different optimization levels (-O0, -O1, -O2, -O3) and compare the generated assembly.
    ```bash
    gcc -O0 sample.c -o sample_O0
    gcc -O2 sample.c -o sample_O2
    ```
* **`Windows`**:
    ```powershell
    cl /c sample.c -o sample.obj
    link sample.obj -o sample.exe
    ```

## 1. Hello World
`Practice` : **Function prologue/epilogue** and **External library calls**
```c
#include <stdio.h>

int main() {
    printf("Hello World\n");
    return 0;
}
```

## 2. Add Two Numbers

`Practice`: **Integer arithmetic** and **Register usage**

```c
#include <stdio.h>

int main() {
    int a = 10, b = 20;
    printf("%d\n", a + b);
    return 0;
}
```

## 3. If Statement
`Practice`: **CMP** and **Conditional jumps**

```c
#include <stdio.h>

int main() {
    int x = 15;

    if (x > 10)
        puts("Large");
    else
        puts("Small");
    return 0;
}
```

## 4. Nested If

`Practice`: **Nested branches**

```c
#include <stdio.h>

int main() {
    int x = 20;

    if (x > 10) {
        if (x < 30)
            puts("Range");
    }
    return 0;
}
```
## 5. For Loop

`Practice`: **Loop control variables**

```c
#include <stdio.h>

int main() {
    for (int i = 0; i < 5; i++)
        printf("%d\n", i);
    return 0;
}
```

