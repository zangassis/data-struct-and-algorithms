## Palindrome 1

```csharp
public class Solution {
    public bool IsPalindrome(string s) {
        if(string.IsNullOrEmpty(s))
            return true;
        
        string cleanText = new string(s
            .Where(char.IsLetterOrDigit)
            .ToArray())
            .ToLower();

        int min = 0;
        int max = cleanText.Length - 1;

        while(min < max)
        {
            if(cleanText[min] != cleanText[max])
                return false;
            min++;
            max--;
        }
        return true;
    }
}
```