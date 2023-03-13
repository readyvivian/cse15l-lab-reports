# Week 9 Lab Report

Vivian Wang    A17457779    v8wang@ucsd.edu

## Researching Command: `find`

### `-name`

This option finds file by name. It is probably the most commonly used command.

* Example 1: This option is useful in this example because it specifically finds files with name "ch1.txt" in the current working directory. It finds five files that match.
  ```
  % find . -name ch1.txt
  ./non-fiction/OUP/Berk/ch1.txt
  ./non-fiction/OUP/Abernathy/ch1.txt
  ./non-fiction/OUP/Rybczynski/ch1.txt
  ./non-fiction/OUP/Kauffman/ch1.txt
  ./non-fiction/OUP/Fletcher/ch1.txt
  ```

* Example 2: This option is useful in this example because it specifically finds files with name "WhereToParis.txt" in the current working directory. It finds no file that matches.
  ```
  % find . -name WhereToParis.txt
  ```

### `-type`

This option finds file by type, such as regular files, directories, or symlinks.

* Example 1: This option is useful in this example beacause it finds all directories in the current working directory. It finds twelve directories.
  ```
  % find . -type d
  .
  ./non-fiction
  ./non-fiction/OUP
  ./non-fiction/OUP/Berk
  ./non-fiction/OUP/Abernathy
  ./non-fiction/OUP/Rybczynski
  ./non-fiction/OUP/Kauffman
  ./non-fiction/OUP/Fletcher
  ./non-fiction/OUP/Castro
  ./travel_guides
  ./travel_guides/berlitz1
  ./travel_guides/berlitz2
  ```

* Example 2: This option is useful in this example because it finds all regular files in the directory `non-fiction/OUP/Berk`. It finds four regular files.
  ```
  % find non-fiction/OUP/Berk -type f
  non-fiction/OUP/Berk/ch2.txt
  non-fiction/OUP/Berk/ch1.txt
  non-fiction/OUP/Berk/CH4.txt
  non-fiction/OUP/Berk/ch7.txt
  ```

### `-size`

This option finds file by size. It allows you to search for files that are exactly greater than, or less than a specific size.

* Example 1: This option is useful in this example because it finds all regular files that are exactly 39,905 bytes. It finds one file that matches.
  ```
  % find . -type f -size 39905c
  ./non-fiction/OUP/Abernathy/ch14.txt
  ```

* Example 2: This option is useful in this example because it finds all regular files that are less than 2 kilobytes. It finds ten files that matches.
  ```
  % find . -type f -size -2k
  ./travel_guides/berlitz1/HandRLasVegas.txt
  ./travel_guides/berlitz1/HandRIstanbul.txt
  ./travel_guides/berlitz1/HandRHongKong.txt
  ./travel_guides/berlitz1/HandRLisbon.txt
  ./travel_guides/berlitz1/HandRMallorca.txt
  ./travel_guides/berlitz1/HandRLosAngeles.txt
  ./travel_guides/berlitz1/HandRMadeira.txt
  ./travel_guides/berlitz1/HandRIbiza.txt
  ./travel_guides/berlitz1/HandRLakeDistrict.txt
  ./travel_guides/berlitz1/HandRJerusalem.txt

### `-mtime`

This option finds file by last modification time. It allows you to search for files that have a modification time exactly, greater than, or less than a specific time.

* Example 1: This option is useful in this example beacause it finds all directories in the directory `non-fiction/OUP/Abernathy` that are modified in the last 28 days. It finds ten files that match.
  ```
  % find non-fiction/OUP/Abernathy -mtime 28
  non-fiction/OUP/Abernathy
  non-fiction/OUP/Abernathy/ch2.txt
  non-fiction/OUP/Abernathy/ch3.txt
  non-fiction/OUP/Abernathy/ch1.txt
  non-fiction/OUP/Abernathy/ch7.txt
  non-fiction/OUP/Abernathy/ch6.txt
  non-fiction/OUP/Abernathy/ch8.txt
  non-fiction/OUP/Abernathy/ch9.txt
  non-fiction/OUP/Abernathy/ch15.txt
  non-fiction/OUP/Abernathy/ch14.txt

* Example 2: This option is useful in this example beacause it finds all directories in the directory `travel_guides/berlitz1` that are modified 30 or more days ago. It finds no file that matches.
  ```
  % find travel_guides/berlitz1 -mtime +30
  ```

### Resource:

https://linuxize.com/post/how-to-find-files-in-linux-using-the-command-line/

