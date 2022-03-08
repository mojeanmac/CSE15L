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
![Image](03.png)
- Which implementation is correct?

- Describe the bug:

## Test 2:
```
[link](foo(and(bar))
```
![Image](04.png)
- Which implementation is correct?

- Describe the bug: