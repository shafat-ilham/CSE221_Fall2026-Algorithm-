# Mergesort Algorithm

- base case len(arr)<=1, no need to sort, just return the array!
- split the arrays midway
- send in the same function to sort
- merge and return.

```java
public static int[] mergesort(int[] arr){
    int len = arr.length;
    if(len<=1) return arr; // base case
    int mid = len/2;
    int[] x = Arrays.copyOfRange(arr, 0, mid); //221 allows some certain functions in this course.
    int[] y = Arrays.copyOfRange(arr, mid, len);
    return merge(mergesort(x),mergesort(y)); // merge the sorted arrays.
}
