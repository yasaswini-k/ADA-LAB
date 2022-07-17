// Quick sort in C

#include <stdio.h>
#include <stdlib.h>
 #include<time.h>

void swap(int *a, int *b) {
  int t = *a;
  *a = *b;
  *b = t;
}

int partition(int array[], int low, int high) {

  int pivot = array[high];
  
  int i = (low - 1);

  for (int j = low; j < high; j++) {
    if (array[j] <= pivot) {
   
      i++;
     
      swap(&array[i], &array[j]);
    }
  }

  swap(&array[i + 1], &array[high]);
  
  return (i + 1);
}

void quickSort(int array[], int low, int high) {
  if (low < high) {
   
    int pi = partition(array, low, high);
   
    quickSort(array, low, pi - 1);
    
    quickSort(array, pi + 1, high);
  }
}

void printArray(int array[], int size) {
  for (int i = 0; i < size; ++i) {
    printf("%d  ", array[i]);
  }
  printf("\n");
}

int main() {
    int m,i;
  int ar[3000];
  time_t start, end;
  printf("enter the number");
    scanf("%d",&m);
  for(i=0;i<m;i++)
  {
      ar[i]=rand();
  }
  start=time(NULL);
  int n = sizeof(ar) / sizeof(ar[0]);
  
  printf("Unsorted Array\n");
  printArray(ar, n);
 
  quickSort(ar, 0, n - 1);
  
  printf("Sorted array in ascending order: \n");
  printArray(ar,n);
  end=time(NULL);
  printf("time taken %f", difftime(end,start));
}
