#include <math.h>
#include <stdio.h>
#include <stdlib.h>
void swap(int *a, int *b) {
  int temp = *a;
  *a = *b;
  *b = temp;
}

void heapify(int arr[], int n, int i) {
  int largest = i;
  int l = 2 * i + 1;
  int r = 2 * i + 2;

  if (l < n && arr[l] > arr[largest]) {
    largest = l;
  }

  if (r < n && arr[r] > arr[largest]) {
    largest = r;
  }

  if (largest != i) {
    swap(&arr[i], &arr[largest]);
    heapify(arr, n, largest);
  }
}

void heap(int arr[], int n) {
  int i;
  printf("Initially unsorted array: ");
  for (i = 0; i < n; i++) {
    printf("%d ", arr[i]);
  }
  for (int i = n / 2 - 1; i >= 0; i--) {
    heapify(arr, n, i);
  }

  for (int i = n - 1; i > 0; i--) {
    swap(&arr[0], &arr[i]);
    heapify(arr, i, 0);
  }
  printf("\nFinal sorted array: ");
  for (i = 0; i < n; i++) {
    printf("%d ", arr[i]);
  }
}

void bubble(int arr[], int n) {
  int i, j, m;
  printf("\t\t\tBubble Sorting\n");
  printf("Initially unsorted array: ");
  for (i = 0; i < n; i++) {
    printf("%d ", arr[i]);
  }
  for (i = 0; i < n - 1; i++) {
    for (j = 0; j < n - i - 1; j++) {
      if (arr[j] > arr[j + 1]) {
        swap(&arr[j], &arr[j + 1]);
      }
    }
    printf("\nPass %d: ", i + 1);
    for (m = 0; m < n; m++) {
      printf("%d ", arr[m]);
    }
  }
}
void selection(int arr[], int n) {
  int i, j, min, m;
  printf("\t\t\tSelection Sorting\n");
  printf("Intially unsorted array: ");
  for (i = 0; i < n; i++) {
    printf("%d ", arr[i]);
  }
  for (i = 0; i < n - 1; i++) {
    min = i;
    for (j = i + 1; j < n; j++) {
      if (arr[j] < arr[min])
        min = j;
    }
    if (min != i) {
      swap(&arr[i], &arr[min]);
    }
    printf("\nPass %d: ", i + 1);
    for (m = 0; m < n; m++) {
      printf("%d ", arr[m]);
    }
  }
}
void insertion(int arr[], int n) {
  int i, j, m, temp;
  printf("\t\t\tInsertion Sorting\n");
  printf("Intially unsorted array: ");
  for (i = 0; i < n; i++) {
    printf("%d ", arr[i]);
  }
  for (i = 1; i < n; i++) {
    temp = arr[i];
    j = i - 1;
    while (j >= 0 && arr[j] > temp) {
      arr[j + 1] = arr[j];
      j--;
    }
    arr[j + 1] = temp;
    printf("\nPass %d: ", i);
    for (m = 0; m < n; m++) {
      printf("%d ", arr[m]);
    }
  }
}

int main() {
  int n, i, choice;
  char c;
  while (1) {
    system("clear");
    printf("\nEnter the size of the unsorted array\n");
    scanf("%d", &n);
    int arr[n];
    printf("Enter the values in the array\n");
    for (i = 0; i < n; i++) {
      scanf("%d", &arr[i]);
    }
    system("clear");

    printf("Choose which sorting algorithm you want to use!!\n");
    printf("1. Selection Sort\n2. Insertion Sort\n3.Bubble Sort\n");
    printf("4. Heap Sort\n5.Exit\n");
    scanf("%d", &choice);

    switch (choice) {
    case 1:
      selection(arr, n);
      getchar();
      break;
    case 2:
      insertion(arr, n);
      getchar();
      break;
    case 3:
      bubble(arr, n);
      getchar();
      break;

    case 4:
      heap(arr, n);
      getchar();
      break;
    case 5:
      exit(0);
    }
    getchar();
    printf("\nWould you like to continue? (y/n)\n");
    scanf("%c", &c);
    if (c == 'n')
      return 0;
  }
  return 0;
}
