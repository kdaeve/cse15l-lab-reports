# CSE Lab Report5

## Tests With Different Results

`diff CSE15L-RoseateSpoonbill/output.txt quiz-markdown/markdown-parse/results.txt` <br />

Using `diff` command is the way that I found the differences. `diff` compared the file that was generated from running a make test in the group implementation and then the file from running the commonmark markdown-parse implementation. The outcome showed me what was in our group result for a certain line number followed by a `---` and the common mark result. Next, I used vim by opening .txt files to find which test corresponds to the line number and using `:set number` searching for the line number by arrow keys.  

## Test #1: 194.md on line 212
