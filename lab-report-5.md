# Lab Report 5, Week 10

## How I found the tests:
![Image](01.png)
- I was able to find the difference between the outputs by using `diff` to compare the text files containing the outputs of both markdown-parse repositories.
- Then, I used grep to find the test for the matching output, including the line before that prints the test name.
![Image](02.png)

## Test 1: 194.md
```
[Foo*bar\]]:my_(url) 'title (with parens)'

[Foo*bar\]]
```
View the file [here](194.html)
![Image](03.png)
1. Which implementation is correct?
- It appears that neither is correct according to VScode's implementation:
![Image](05.png)
2. Describe the bug:
- According to [https://www.markdownguide.org/basic-syntax/](https://www.markdownguide.org/basic-syntax/), a link title can be created by wrapping it in singe quotes (`'`) if the brackets are followed by a colon (`:`)
- This means that the actual link should be `my_(url)`
- To fix this, we would need to account for these types of links by checking for a colon after the brackets and finding the link before the bounds of the link title
## Test 2: 496.md
```
[link](foo(and(bar))
```
View the file [here](496.html)
![Image](04.png)
1. Which implementation is correct?
- Joe's implementation is correct because no links are found by VScode:
![Image](06.png)

2. Describe the bug: