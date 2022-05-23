# cpplint

比较死板，style只能按照google style来。

```c
int main()
{
    return 0;
}
```

cpplint会报错：

`{ should almost always be at the end of the previous line [whitespace/braces]`

因为按照google style，\`{\`只能写在一行的最后。
