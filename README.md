`Entry point`

```c
00F10126 | E8 56020000              | call putty.F10381                       |
00F1012B | E9 7AFEFFFF              | jmp putty.F0FFAA                        |
00F10130 | 55                       | push ebp                                |
```

`Code cave`

```c
00F38200 | 0000                     | add byte ptr ds:[eax],al                |
```

Change entry point and jump to code cave that contains the shell code that we’ll paste.

![Untitled](img1.png)

`Shell code`

![Untitled](img2.png)

Then added an instruction where it’ll go back to the main program so it’ll become a Trojan.

![Untitled](img3.png)

`POPFD Address`

```c
00E53B95 | 9D                       | popfd                                   |
```

I also removed the exit instruction and make it jump on POPFD address so the trojan will execute correctly.
![Untitled](img4.png)

Screenshot
![Untitled](img5.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/57908592-c957-480d-89fc-eabd44c65a07/97adec40-af34-4410-9588-14006e83b632/Untitled.png)

**Screenshot**

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/57908592-c957-480d-89fc-eabd44c65a07/61b10792-33b1-46e4-bb5d-4190b4efc5f3/Untitled.png)
