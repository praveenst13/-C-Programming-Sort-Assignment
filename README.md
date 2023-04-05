# C-Programming-Sort-Assignment

## AIM:

To sort the elements by using the method of bubble sort ,insertion sort ,selection sort in C program.
Materials Required:

Hardware: pc with 'c' compiler
## Algorithm:
## Bubble sort:

Bubble sort is a simple sorting algorithm that repeatedly steps through the list to be sorted, compares each pair of adjacent items and swaps them if they are in the wrong order. The pass through the list is repeated until the list is sorted.
Steps for Bubble Sort:

   1. Start with the first element and compare it with the second element. If the first element is greater than the second element, then swap them.
   2. Move to the second element and compare it with the third element. If the second element is greater than the third element, then swap them.
   3. Repeat the above steps until you reach the end of the array.
   4. Now, the largest element in the array is at the last position.
   5. Repeat the above steps again for the remaining elements of the array, for (n-1) elements.

## Insertion sort:

Insertion sort is a simple sorting algorithm that builds the final sorted array one item at a time. It is much less efficient on large lists than more advanced algorithms such as quicksort, heapsort, or merge sort.
Steps for Insertion Sort:

   1. Start with the second element and compare it with the first element. If the second element is smaller than the first element, then swap them.
   2. Move to the third element and compare it with the second element. If the third element is smaller than the second element, then swap them. Also, compare the third element with the first element and swap if necessary.
   3. Repeat the above steps until you reach the end of the array.
   4. Now, the first two elements of the array are sorted.
   5. Repeat the above steps for the remaining elements of the array, i.e., for (n-1) elements.

## Selection Sort:

Selection Sort works by finding the minimum element from the unsorted part of the array and putting it at the beginning.
Steps for the Selection Sort:

    1. Find the minimum element in the unsorted part of the array.
    2. Swap the minimum element with the first element of the unsorted part of the array.
    3.Repeat step 1 and 2 for the remaining unsorted part of the array.

## Code:
Bubble sort:
```
# Code developed : praveen s
# Reg-no : 212222240077

#include <stdio.h>

void bubbleSort(int a[], int n) {
    int i, j, temp;
    for (i = 0; i < n-1; i++) {
        for (j = 0; j < n-i-1; j++) {
            if (a[j] > a[j+1]) {
                temp = a[j];
                a[j] = a[j+1];
                a[j+1] = temp;
            }
        }
    }
}

int main() {
    int a[] = {46, 90, 35, 21, 6, 18, 34};
    int n = sizeof(a)/sizeof(a[0]);
    bubbleSort(a, n);
    printf("Array before sort: \n46, 90, 35, 21, 6, 18, 34\n\n");
    printf("Sorted array: \n");
    for (int i = 0; i < n; i++) {
        printf("%d ", a[i]);
    }
    return 0;
}
```
Insertion sort:
```
# Code developed : praveen s
# Reg-no : 212222240077

#include <stdio.h>

void insertionSort(int a[], int n) {
    int i, key, j;
    for (i = 1; i < n; i++) {
        key = a[i];
        j = i - 1;
        while (j >= 0 && a[j] > key) {
            a[j+1] = a[j];
            j = j - 1;
        }
        a[j+1] = key;
    }
}

int main() {
    int a[] = {46, 90, 35, 21, 6, 18, 34};
    int n = sizeof(a)/sizeof(a[0]);
    insertionSort(a, n);
    printf("Array before sort: \n46, 90, 35, 21, 6, 18, 34\n");
    printf("\nSorted array: \n");
    for (int i = 0; i < n; i++) {
        printf("%d ", a[i]);
    }
    return 0;
}

```
Selection sort:
```

# Code developed : praveen s
# Reg-no : 212222240077


#include <stdio.h>

void selection_sort(int arr[], int n) {
    int i, j, min_idx, temp;
    
    for (i = 0; i < n-1; i++) {
        min_idx = i;
        for (j = i+1; j < n; j++) {
            if (arr[j] < arr[min_idx]) {
                min_idx = j;
            }
        }
        temp = arr[i];
        arr[i] = arr[min_idx];
        arr[min_idx] = temp;
    }
}

int main() {
    int arr[] = {46, 90, 35, 21, 6, 18, 34};
    int n = sizeof(arr)/sizeof(arr[0]);
    int i;
    
    printf("Original array: ");
    for (i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }
    
    selection_sort(arr, n);
    
    printf("\n\nSorted array: ");
    for (i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }
    
    return 0;
}
```

## Output:
Bubble sort:

![img](https://user-images.githubusercontent.com/118707363/230113149-b7c5af13-ffbd-4f38-bae8-09b1133b4059.png)


Insertion sort:

![img](https://user-images.githubusercontent.com/118707363/230113178-b918204d-f012-423d-86e9-442eae8fd068.png)


Selection sort:

![select](https://user-images.githubusercontent.com/118707363/230112585-27c98338-6a8f-47e2-b8f4-f366b0d9b7db.png)

## Result:

Thus the program for sorting the elements is successfully executed.
