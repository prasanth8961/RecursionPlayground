# RECURSION PROBLEMS WITH SOLUTION

Welcome to the **RecursionPlayground Repository**! This repository contains a collection of solutions to problems using recursion, a fundamental concept in programming and computer science.

## About
Recursion is a powerful technique where a function calls itself to solve smaller instances of a problem. This repository aims to:

- Provide solutions for common recursion problems.
- Serve as a practice ground for mastering recursive techniques.
- Explore advanced concepts and optimizations related to recursion.

## Contents

- **Basic Problems**: Simple recursive problems.
- **Intermediate Problems**: Moderately complex problems.
- **Advanced Problems**: Challenging problems requiring a deeper understanding of recursion.

## Examples

### Recursion with Strings

#### 1. String Reverse
```java
public class StringReverse {
    public static String reverse(String str) {
        if (str.isEmpty()) {
            return str;
        }
        return reverse(str.substring(1)) + str.charAt(0);
    }

    public static void main(String[] args) {
        System.out.println(reverse("recursion"));
    }
}
```
**Sample Output:**
```
noisrucer
```

#### 2. Palindrome Check
```java
public class PalindromeCheck {
    public static boolean isPalindrome(String str) {
        if (str.length() <= 1) {
            return true;
        }
        if (str.charAt(0) != str.charAt(str.length() - 1)) {
            return false;
        }
        return isPalindrome(str.substring(1, str.length() - 1));
    }

    public static void main(String[] args) {
        System.out.println(isPalindrome("level"));
        System.out.println(isPalindrome("world"));
    }
}
```
**Sample Output:**
```
true
false
```

### Recursion with Numbers

#### 1. Decimal to Binary
```java
public class DecimalToBinary {
    public static String toBinary(int n) {
        if (n == 0) {
            return "";
        }
        return toBinary(n / 2) + (n % 2);
    }

    public static void main(String[] args) {
        System.out.println(toBinary(10));
    }
}
```
**Sample Output:**
```
1010
```

#### 2. Sum of Natural Numbers
```java
public class SumOfNaturalNumbers {
    public static int sum(int n) {
        if (n == 0) {
            return 0;
        }
        return n + sum(n - 1);
    }

    public static void main(String[] args) {
        System.out.println(sum(5));
    }
}
```
**Sample Output:**
```
15
```

### Divide and Conquer

#### 1. Binary Search
```java
public class BinarySearch {
    public static int search(int[] arr, int low, int high, int key) {
        if (low > high) {
            return -1;
        }
        int mid = (low + high) / 2;
        if (arr[mid] == key) {
            return mid;
        } else if (key < arr[mid]) {
            return search(arr, low, mid - 1, key);
        } else {
            return search(arr, mid + 1, high, key);
        }
    }

    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 4, 5};
        System.out.println(search(arr, 0, arr.length - 1, 3));
    }
}
```
**Sample Output:**
```
2
```

#### 2. Fibonacci
```java
public class Fibonacci {
    public static int fib(int n) {
        if (n <= 1) {
            return n;
        }
        return fib(n - 1) + fib(n - 2);
    }

    public static void main(String[] args) {
        System.out.println(fib(6));
    }
}
```
**Sample Output:**
```
8
```

#### 3. Merge Sort
```java
public class MergeSort {
    public static void mergeSort(int[] arr, int left, int right) {
        if (left < right) {
            int mid = (left + right) / 2;
            mergeSort(arr, left, mid);
            mergeSort(arr, mid + 1, right);
            merge(arr, left, mid, right);
        }
    }

    private static void merge(int[] arr, int left, int mid, int right) {
        int n1 = mid - left + 1;
        int n2 = right - mid;
        int[] L = new int[n1];
        int[] R = new int[n2];

        for (int i = 0; i < n1; i++) L[i] = arr[left + i];
        for (int i = 0; i < n2; i++) R[i] = arr[mid + 1 + i];

        int i = 0, j = 0, k = left;
        while (i < n1 && j < n2) {
            if (L[i] <= R[j]) {
                arr[k++] = L[i++];
            } else {
                arr[k++] = R[j++];
            }
        }

        while (i < n1) arr[k++] = L[i++];
        while (j < n2) arr[k++] = R[j++];
    }

    public static void main(String[] args) {
        int[] arr = {12, 11, 13, 5, 6, 7};
        mergeSort(arr, 0, arr.length - 1);
        for (int num : arr) System.out.print(num + " ");
    }
}
```
**Sample Output:**
```
5 6 7 11 12 13
```

### Graph Traversals

#### BFS
```java
// BFS 
```
**Sample Output:**
```

```

#### DFS
```java
// DFS 
```
**Sample Output:**
```

```
