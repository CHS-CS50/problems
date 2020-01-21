# Problem: Whodunit

## tl;dr

Answer some questions and then implement a program that reveals a reveals a hidden message in a BMP, per the below.

```
$ ./whodunit clue.bmp verdict.bmp
```

{% next %}

# Getting Ready

- First, curl up with Doug’s shorts on [file pointers](https://youtu.be/bOF-SpEAYgk) and [structs](https://youtu.be/N5pA7RvvQDg).

- Next, review ([from lecture](https://youtu.be/ed2lnJNf7HU)) David’s introduction to `valgrind`, a command-line tool that will help you find "memory leaks": memory that you’ve allocated (i.e., asked the operating system for), as with `malloc`, but not freed (i.e., given back to the operating system).

- Finally, [remind yourself](https://youtu.be/VtkMZjvvKaU) how `debug50` works if you’ve forgotten or not yet used! (It’s worth it!)

{% next %}

# Getting Started

Take a look at the code that has been included: a C file, a header file, and four images. Who knows what could be inside those! Let’s get started.

## Background

Welcome to Tudor Mansion. Your host, Mr. John Boddy, has met an untimely end—he’s the victim of foul play. To win this game, you must determine whodunit.

Unfortunately for you (though even more unfortunately for Mr. Boddy), the only evidence you have is a 24-bit BMP file called clue.bmp, pictured below, that Mr. Boddy whipped up on his computer in his final moments. Hidden among this file’s red "noise" is a drawing of whodunit.

![clue.bmp](clue.bmp)



