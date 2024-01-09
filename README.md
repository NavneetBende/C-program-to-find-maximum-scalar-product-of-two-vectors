Maximum Scalar Product in C
Here, in this page we will discuss about the maximum scalar product in C. There we have two arrays array 1 and array 2 so here we need to find dot products of two arrays. Dot product is also known as the scalar product of two vectors.

maximum scalar product
While loop in C
Example
Input :arr1[4] = [10, 30, 40, 20]
            arr2[4] = [2, 4, 5, 1]
Output : 370
Explanation : 10*1 + 20*2 + 30*4 + 40*5 = 370
Algorithm :
Sort the first array in ascending order,
Sort the second array in ascending order.
Declare a variable say product = 0.
Run a loop from index 0 to n
Set product += (arrr1[i]*arr2[i])
After complete iteration print product.
Maximum scalar product in C
Related Pages
Removing Duplicate elements from an array

Finding Minimum scalar product of two vectors

Counting the number of even and odd elements in an array 

Find all Symmetric pairs in an array 

Find maximum product sub-array in a given array

Code in C
Run
#include <stdio.h>

int main(){

   int arr1[] = {1, 2, 6, 3, 7};
   int arr2[] = {10, 7, 45, 3, 7};

   int n = sizeof(arr1)/sizeof(arr1[0]);


   //Sort arr1 in ascending order
   for(int i=0; i<n; i++){
       for(int j=i+1; j<n; j++){ 
           if(arr1[i]>arr1[j]){
               int temp = arr1[i];
               arr1[i] = arr1[j];
               arr1[j] = temp;
           }
       }
   }

   //Sort arr2 in ascending order
   for(int i=0; i<n; i++){
       for(int j=i+1; j<n; j++){ if(arr2[i]>arr2[j]){
                int temp = arr2[i];
                arr2[i] = arr2[j];
                arr2[j] = temp;
           }
       }
    }

    int product = 0;
    for(int i=0; i<n; i++)
        product += arr1[i]*arr2[i];

    printf("%d ", product);

}
Output
413
