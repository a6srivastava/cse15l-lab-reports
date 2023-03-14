#Lab Rep 5 Less command

##less
```
 $ less [options] file_path
```
![hello world](5ss1.png)

1
###using less without any options

```
$ less ~/newdir/lab7/ListExamples.java 
```
![hello world](5ss2.png)
5ss2.png
2
###using less on a file that doesnt exist
```
$ less boogie.txt
```
![hello world](5ss3.png)
5ss3.png
- 
3
###using less with -f
```
$ less -f ~/newdir
```
- this allows for the opening of non text files such as directory and non-regular files
- ![hello world](5ss5.png)
5ss5.png
###using less with -N
```
$ less -Nf ~/newdir/lab7/ListExamples.java 
```
- -N displays line numbers on the left side of the screen.
5ss4.png
![hello world](5ss4.png)
###using less with -S

```
$ less -NfS ~/newdir/lab7/ListExamples.java 
```
- -S chops long lines instead of wrapping them.
5ss6.png
![hello world](5ss6.png)
