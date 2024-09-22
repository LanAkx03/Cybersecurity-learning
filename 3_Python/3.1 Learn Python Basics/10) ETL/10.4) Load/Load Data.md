Python can be used to read data from a variety of places, including databases and files. Two file types that are often used are .txt and .csv. You can import and export files using built-in Python functionality or Python's CSV library. We’ll go through both options!


File modes :

- Read:  `"r"`
- Write:  `"w"`
- Append:  `"a"`
- Read and write:  `"r+"`

To create a new file called “hello.txt” and write “Hello, world!” to it, use the following code:

```python
file = open("hello.txt", "w")
file.write("Hello, world!")
file.close()
```

 You can also use the `**with**` statement to read a file line by line:

```python
with open("file.txt") as f:
    for line in f:
        #do something with line
        print(line)
```

In our example : 

```python
>>> with open("hello.txt") as f:
...     for line in f:
...             print(line)
...
Hello, world!
>>>
```

To exit the pyhon 'mode' 

```python
exit()
```
