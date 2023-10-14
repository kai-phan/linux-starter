# Basic Text-fu

## stdout (standard output)

```bash
$ echo "Hello World" > basic_text_fu/hello_world.txt
```
This command will get the standard output of the echo command and write it to the file hello_world.txt.

```bash
$ echo "Hello World" >> basic_text_fu/hello_world.txt
```
This command will get the standard output of the echo command and append it to the file hello_world.txt.

## stdin (standard input)

```bash
$ cat < basic_text_fu/hello_world.txt > basic_text_fu/hello_world_copy.txt
```
## stderr (standard error)

```bash
$ ls fakedir 2> basic_text_fu/hello_world_error.txt
```

Send stdout and stderr to the same file.

```bash
$ ls > basic_text_fu/hello_world_both.txt 2>&1
```

Breakdown:
- `ls` - the command to run
- `>` - redirect stdout
- `basic_text_fu/hello_world_both.txt` - the file to redirect stdout to
- `2>&1` - redirect stderr to stdout
- `2>` - redirect stderr
- `&1` - redirect to stdout in case the shell is redirecting to a file

Short way
```bash
$ ls fakeDir &> basic_text_fu/hello_world_both.txt
```

Discard stdout and stderr

```bash
$ ls fakedir 2> /dev/null
```

## pipe
The | character is used to pipe the output of one command to the input of another.

```bash
$ ls -la /etc/ | less
```

## tee
The tee command reads standard input and writes it to both standard output and one or more files.

```bash
$ ls -la /etc/ | tee basic_text_fu/tee.txt
```

## env
The env command is used to display all environment variables.

```bash
$ env
```

## cut
The cut command is used to extract sections from each line of input.

```bash
$ cut [-c | -f | -d] [file]
```

- -c : character
- -f : field
- -d : delimiter

Extract the first 5 characters
```bash
$ cut -c 1-5 basic_text_fu/sample.txt
```
Extract the first 5 characters
```bash
$ cut -c -5 basic_text_fu/sample.txt
```
Extract the characters from index 5
```bash
$ cut -c 5- basic_text_fu/sample.txt
```
Extract content by the field, TAB is the default delimiter
```bash
$ cut -f 2 basic_text_fu/sample.txt
```
Extract content by the field, using ; as the delimiter
```bash
$ cut -f 1 -d ";" basic_text_fu/sample.txt
```

## paste
The paste command is used to merge lines of files.

```bash
$ paste [-s | -d] [file1] [file2]
```

- -s : serial
- -d : delimiter

Merge lines of files
```bash
$ paste -s -d ' ' basic_text_fu/sample.txt basic_text_fu/sample2.txt
```

## head
The head command is used to output the first part of files.

```bash
$ head [-n | -c] [file]
```

- -n : number of lines
- -c : number of bytes

Output the first 2 lines
```bash
$ head -n 2 basic_text_fu/sample2.txt
```

```bash
$ head -n 10 /var/log/system.log
```

## tail
The tail command is used to output the last part of files.

```bash
$ tail [-n | -c | -f] [file]
```

- -n : number of lines
- -c : number of bytes
- -f : follow

## expand and unexpand
The expand command is used to convert tabs to spaces.

```bash
$ expand [file]
```

The unexpand command is used to convert spaces to tabs.

```bash
$ unexpand [file]
```

## grep
The grep command is used to search for text patterns.

```bash
$ grep [-i | -v | -c | -n | -l | -r | -e | -f] [pattern] [file]
```

- -i : ignore case
- -v : invert match
- -c : count
- -n : line number
- -l : file name
- -r : recursive
- -e : regular expression
- -f : fixed string

Search for the pattern "root" in the file /etc/passwd
```bash
$ grep root /etc/passwd
```

Search for the pattern "root" in the file /etc/passwd, ignore case
```bash
$ grep -i root /etc/passwd
```

Search for the pattern "root" in the file /etc/passwd, invert match
```bash
$ grep -v root /etc/passwd
```

Search for the pattern "root" in the file /etc/passwd, count
```bash
$ grep -c root /etc/passwd
```

Search for the pattern "root" in the file /etc/passwd, line number
```bash
$ grep -n root /etc/passwd
```

Search for the pattern "root" in the file /etc/passwd, file name
```bash
$ grep -l root /etc/passwd
```

Search for the pattern "root" in the file /etc/passwd, recursive
```bash
$ grep -r root /etc/
```

Pipe the output of the ls command to the grep command
```bash
$ ls -la /etc/ | grep -n root
```