###389 Find the Difference

Given two strings s and t which consist of only lowercase letters.
String t is generated by random shuffling string s and then add one more letter at a random position.
Find the letter that was added in t.
Example:

Input:
s = "abcd"
t = "abcde"

Output:
e

Explanation:
'e' is the letter that was added.


Subscribe to see which companies asked this question


Show Tags

Hash Table
Bit Manipulation



Show Similar Problems

 (E) Single Number



Given two strings s and t which consist of only lowercase letters.String t is generated by random shuffling string s and then add one more letter at a random position.Find the letter that was added in t.Example:

Input:
s = "abcd"
t = "abcde"

Output:
e

Explanation:
'e' is the letter that was added.

Input:
s = "abcd"
t = "abcde"

Output:
e

Explanation:
'e' is the letter that was added.
Subscribe to see which companies asked this question
###Solution
```java
public class Solution {
    public char findTheDifference(String s, String t) {
        
        int [] alphaS = new int[26];
        int [] alphaT = new int[26];
        
        int i = 0;
        for(;i < s.length(); i ++){
            alphaS[s.charAt(i) -'a']++;
            alphaT[t.charAt(i) -'a']++;
        }
        alphaT[t.charAt(i) -'a']++;
        
        
        for(i = 0; i < 26; i ++){
            if(alphaS[i] != alphaT[i])
                return (char)('a'+i);
        }
        
        return 'a';
    }
}