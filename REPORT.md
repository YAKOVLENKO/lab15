## Laboratory work XV

Данная лабораторная работа посвещена изучению инструментов статического и динамического анализа кода
```ShellSession
$ open http://cppcheck.sourceforge.net
```

## Tasks

- [X] 1. Ознакомиться со ссылками учебного материала
- [X] 2. Используя **cpplint** провести анализ проекта на **C++**
- [X] 3. Используя **Cppcheck** провести анализ проекта на **C++**
- [X] 4. Используя **OCLint** провести анализ проекта на **C++**
- [X] 5. Используя **Valgrind** провести анализ проекта на **C++**
- [X] 6. Составить отчет и отправить ссылку личным сообщением в **Slack**

## Выполнение задания
**cpplint**
```
$ cpplint main.cpp

main.cpp:0:  No copyright message found.  You should have a line: "Copyright [year] <Copyright Owner>"  [legal/copyright] [5]
main.cpp:4:  Line ends in whitespace.  Consider deleting these extra spaces.  [whitespace/end_of_line] [4]
main.cpp:4:  Redundant blank line at the start of a code block should be deleted.  [whitespace/blank_line] [2]
Done processing main.cpp
Total errors found: 3

```
**Cppcheck**
```
$ cppcheck main.cpp

Checking main.cpp...
```
**OCLint**
```
$ oclint main.cpp -- -c


OCLint Report

Summary: TotalFiles=1 FilesWithViolations=0 P1=0 P2=0 P3=0 


[OCLint (http://oclint.org) v0.13]
```
**Valgrind**
```
$ valgrind ./main
==21914== Memcheck, a memory error detector
==21914== Copyright (C) 2002-2017, and GNU GPL'd, by Julian Seward et al.
==21914== Using Valgrind-3.13.0 and LibVEX; rerun with -h for copyright info
==21914== Command: ./main
==21914== 
Hello, World!
==21914== 
==21914== HEAP SUMMARY:
==21914==     in use at exit: 72,704 bytes in 1 blocks
==21914==   total heap usage: 2 allocs, 1 frees, 73,728 bytes allocated
==21914== 
==21914== LEAK SUMMARY:
==21914==    definitely lost: 0 bytes in 0 blocks
==21914==    indirectly lost: 0 bytes in 0 blocks
==21914==      possibly lost: 0 bytes in 0 blocks
==21914==    still reachable: 72,704 bytes in 1 blocks
==21914==         suppressed: 0 bytes in 0 blocks
==21914== Rerun with --leak-check=full to see details of leaked memory
==21914== 
==21914== For counts of detected and suppressed errors, rerun with: -v
==21914== ERROR SUMMARY: 0 errors from 0 contexts (suppressed: 0 from 0)
```


## Links

- [Google C++ Style Guide](https://github.com/cpplint/cpplint)
- [Cppcheck Manual](http://cppcheck.sourceforge.net/manual.pdf)
- [Valgrind Quick Start Guide](http://valgrind.org/docs/manual/index.html)
- [OCLint Tutorial](http://docs.oclint.org/en/stable/intro/tutorial.html)

```
Copyright (c) 2017 Братья Вершинины
```


