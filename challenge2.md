```
public static int Solution(string S)
{
    int max = 0;
    var sentences = S.Split(new char[] { '.', '?', '!' });

    foreach (var sentence in sentences)
    {
        //int length = sentence.Split(' ', StringSplitOptions.RemoveEmptyEntries).Length;
        int length = sentence.Split(' ').Where(t => !string.IsNullOrEmpty(t)).Count();
        if (length > max)
            max = length;
    }

    return max;
}
```
