# Palindrome String
### Given a string s, the task is to check if it is palindrome or not.

## Example:
```
    Input: s = “abba”
    Output: 1
    Explanation: s is a palindrome

    Input: s = “abc” 
    Output: 0
    Explanation: s is not a palindrome
```

<img src ="https://media.geeksforgeeks.org/wp-content/uploads/20240920165631/Check-for-Palindromic-String.webp">

# Code 
```
#include <bits/stdc++.h>
using namespace std;

// Function to check if a string is a palindrome
int isPalindrome(string & s){

    // Initialize two pointers: one at the beginning (left)
    // and one at the end (right)
    int left = 0;
    int right = s.length() - 1;

    // Continue looping while the two pointers
    //  have not crossed each other
    while (left < right)
    {

        // If the characters at the current positions are not equal,
        // return 0 (not a palindrome)
        if (s[left] != s[right])
            return 0;

        // Move the left pointer to the right
        // and the right pointer to the left
        left++;
        right--;
    }

    // If no mismatch is found,
    // return 1 (the string is a palindrome)
    return 1;
}

int main(){
    string s = "abba";
    cout << isPalindrome(s) << endl;

    return 0;
}
```

# Output
```
1
```
# Complexity
Time Complexity: O(n), where n is the length of the input string.
<br>
Auxiliary Space: O(1), no extra data structures used. 
