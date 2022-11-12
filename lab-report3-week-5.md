# <span style="color:teal"> Week 5 Lab Report 3 </span>

<span style="font-family:Hellvetica; font-size:1em;">Welcome to CSE15L Lab Report 3! Today, I'm experimenting with the "grep" command on the command line with the different options that it has.</span>

```
grep
```

<span style="font-family:Hellvetica; font-size:1em;">The grep command is useful for searching a file or multiple files for a given strength and printing that line</span>

## <span style="color:Magenta"> 1) -b</span>

```
grep "weather" technical/911report/chapter-1.txt
```

![image](grep-weather.jpg)

<span style="font-family:Hellvetica; font-size:1em;">As you can see, when I run that command, it prints out the line in that text file that has the string that I'm searching for. In this example, I'm using "weather" which is highlighted orange above. Now that I've tested grep by default, I'm going to start using different command line options that go with grep to see their effect. The first one I'll be looking at is "-b".</span>

```
grep -b "danger" technical/911report.*.txt
```
![image](grep-b-1.jpg)
<span style="font-family:Hellvetica; font-size:1em;">All instances of the word "danger" are highlighted and displayed in the contents of the files we searched through</span>

```
grep -b "looking" technical/911report.*.txt
```
![image](grep-b-2.jpg)
<span style="font-family:Hellvetica; font-size:1em;">All instances of the word "looking" are highlighted and displayed in the contents of the files we searched through</span>

```
grep -b "weather" technical/911report.*.txt
```
![image](grep-b-3.jpg)
<span style="font-family:Hellvetica; font-size:1em;">All instances of the word "weather" are highlighted and displayed in the contents of the files we searched through</span>

## <span style="color:Magenta"> What It Does</span>

<span style="font-family:Hellvetica; font-size:1em;">What "-b" does with grep is it not only prints out the whole line where the string you're looking for is located, but it prints out the file name (with the directory) and the line number. This is pretty useful when trying to track down the specific areas in a text file that have a word or phrase that you're looking for. Think of this as also like Ctrl+F on a PDF in a web browser.</span>


## <span style="color:Magenta"> 2) -h</span>
```
grep - h <input> <path>
```
<span style="font-family:Hellvetica; font-size:1em;">The next command option I'll be looking at is "-h". </span>
```
grep - h "weather" technical/911report/*.txt
```
![image](grep-h-1.jpg)
<span style="font-family:Hellvetica; font-size:1em;">By using -h here, all instances of the "weather" are displayed and highlighted. This is displaying it in the format of the file's contents which differs from -b where it has the file name and line number on the left side. </span>
```
grep - h "looking" technical/911report/*.txt
```
![image](grep-h-2.jpg)
<span style="font-family:Hellvetica; font-size:1em;">By using -h here, all instances of the "looking" are displayed and highlighted. This is displaying it in the format of the file's contents which differs from -b where it has the file name and line number on the left side. </span>
```
grep - h "danger" technical/911report/*.txt
```
![image](grep-h-3.jpg)
<span style="font-family:Hellvetica; font-size:1em;">By using -h here, all instances of the "danger" are displayed and highlighted. This is displaying it in the format of the file's contents which differs from -b where it has the file name and line number on the left side. </span>

## <span style="color:Magenta"> What It Does</span>
<span style="font-family:Hellvetica; font-size:1em;">What "-h" does is printing  out in bulk the text that contains the string you're searching for. This is useful when it comes to identifying and counting how many of that string are present in the txt file or files you're searching for. You can combine this with wc to get a finite answer. It differs from "-b" which has everything displayed in a more left-alligned manner. The usage of "-h" provides a display that shows what the contents look like within the file without being shifted around to fit the parameters of "-b" showing the file name and number.</span>


## <span style="color:Magenta"> 2) -o</span>
<span style="font-family:Hellvetica; font-size:1em;">Lastly, I'll be looking into "-o".</span>
```
grep - h "weather" technical/911report/*.txt
```
![image](grep-o-1.jpg)
<span style="font-family:Hellvetica; font-size:1em;">In this screenshot, every instance of the word weather in the files we're searching for is printed on a new line..</span>
```
grep - h "and" technical/911report/*.txt
```
![image](grep-o-2.jpg)
<span style="font-family:Hellvetica; font-size:1em;">In this screenshot, every instance of the word and in the files we're searching for is printed on a new line.</span>
```
grep - h "looking" technical/911report/*.txt
```
![image](grep-o-3.jpg)
<span style="font-family:Hellvetica; font-size:1em;">In this screenshot, every instance of the word looking in the files we're searching for is printed on a new line.</span>

<span style="font-family:Hellvetica; font-size:1em;">What "-o" does it take each string that you're searching for that's present in the file(s) you're searching in and prints it on a line. So if you have a thousand of that string present, it'll print it out a thousand times. Similarly to "-h", this can be very useful for wc in order to get a finite number of how many of that string are present in the files you're searching in.</span>