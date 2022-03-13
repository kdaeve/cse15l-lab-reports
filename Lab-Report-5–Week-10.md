# CSE Lab Report5

## Tests With Different Results

`diff CSE15L-RoseateSpoonbill/output.txt quiz-markdown/markdown-parse/results.txt` <br />

Using `diff` command is the way that I found the differences. `diff` compared the file that was generated from running a make test in the group implementation and then the file from running the commonmark markdown-parse implementation. The outcome showed me what was in our group result for a certain line number followed by a `---` and the common mark result. Next, I used vim by opening .txt files to find which test corresponds to the line number and using `:set number` searching for the line number by arrow keys.  

## Test #1: 194.md on line 212

On 194.md, the contents shows below:  
``[Foo*bar\]]:my_(url) 'title (with parens)' ``  

Running with command `diff`, and compare our group with markdown that shows:  
![Image](images/lab-report5/diff1.png)  

Basically, our group version in this test file has the correct output. However, this common mark version finds a link incorrectly. Meanwhile, we are expected the correct output should be an empty array since the code should confirm the next character right after `]` is `(`.So, a valid link cannot have other characters between the closing and opening parentheses. Therefore, to fix this bug we need to include another `if` statement that tests for `nextCloseBracket == openParen - 1`.  

We excepted the result of .md file is: `[]`.  

## Test #2: 342.md on line 542
On 194.md, the contents shows below:  
``[not a `link](/foo`) ``  

Running with command `diff`, and compare our group with markdown that shows:  
![Image](images//lab-report5/diff2.png)  

Basically, our group version in this test file has the correct implementation. However, the common mark implementation is incorrect since it ignored the backticks that indicate a code block and included as regular text. A bug in the common mark that I found is it does not omit the text found in code blocks. So, to fix this bug we should have another `if` statement that will check for matching sets of backticks and skip the contents inside when searching for links. Thus, we can fix it by following code:  

```
public static ArrayList<String> getlinks(String markdown) {
    ArrayList<String> toReturn = new ArrayList<>();
    // find the next [, then find the ], then find the (, then take up to
    // the next )
    int currentIndex = 0;
    while (currentIndex < markdown.length()) {
        int nextOpenBracket = markdown.indexof("[", currentIndex);
        int nextCodeBlock = markdown.indexOf("\n```");
        if (nextCodeBlock < nextOpenBracket && nextCodeBlock != -1) {
            int endOfCodeBlock = markdown.indexOf("\n```");
            currentIndex = endOfCodeBlock + 1;
            continue;
            if (nextOpenBracket == -1 || nextCloseBracket == -1
                  || closeParen == -1 || openParen == -1) {
                return toReturn;
            }
        }
    }
}
```
We excepted the result of .md file is: `[]`.  