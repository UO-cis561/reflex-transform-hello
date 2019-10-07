# reflex-transform-hello
A simpler example of writing a simple file-scanning
application with the REflex scanner generator. 

REflex reads hello.lxx and creates lex.yy.cpp. 
You compile lex.yy.cpp to get the file-scanning 
program. 

It should be possible to create this application 
both on your working environment (laptop, etc) 
and in Docker.  Your working environment is more 
convenient, so develop and debug there first before
checking (and possibly debugging) in the Docker environment. 


Pre-requisites:  
RE/flex must be installed in the standard places, 
with a library in /usr/local/lib, include files 
in /usr/local/include/reflex, and 'reflex' on the 
search path.  (The CIS 461 docker file has 
RE/flex installed this way.)

## To build 
(on a Unix system, including MacOS): 

`make`

This will invoke the Makefile in the 'src' directory
and produce a binary in the 'bin' directory. 

## To run
(after building)

`bin/hello < data/example.txt`

The output should be: 
```
Well, goodby mars! Nice to meet you.
I have been looking for a mars much like you,
although there are a few things I might like
to alter.
1 occurrences of hello
2 occurrences of world
```




