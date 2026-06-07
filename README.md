# Reverse a Number

## Problem Statement
Given an integer `n`, reverse its digits and return the reversed number.

### Example

Input:
```
12345
```

Output:
```
54321
```

Input:
```
120
```

Output:
```
21
```

## Approach
1. Extract the last digit using `% 10`.
2. Append it to the reversed number.
3. Remove the last digit using `/ 10`.
4. Repeat until the number becomes `0`.

## Java Solution

```java
public class Main {
    public static int reverseNumber(int n) {
        int rev = 0;

        while (n != 0) {
            int digit = n % 10;
            rev = rev * 10 + digit;
            n /= 10;
        }

        return rev;
    }

    public static void main(String[] args) {
        int n = 12345;
        System.out.println(reverseNumber(n));
    }
}
```

## Complexity Analysis

- **Time Complexity:** O(log₁₀ n)
- **Space Complexity:** O(1)

## Tags
`Math` `Number Manipulation` `Basic Programming`
