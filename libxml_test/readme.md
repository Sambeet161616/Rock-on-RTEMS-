This is just to study and test libxml and gccxml.The installation was by directly building from source for GCCXML.
libxml is already there in most distros.
First a hello.c file was created and it was converted to xml using gccxml.
$gccxml hello.c
It produces a file as required hello.xml,an xml document with root GCCXML.

Then a file is downloaded from http://www.xmlsoft.org/tutorial/apc.html , a tutorial for libxml, called as parse_tut.c. and an
xml file was written to test it as per the code of parse_tut.c

The command to run the  file parse_tut.c is the following

$gcc parse_tut.c $(xml2-config --cflags --libs)

This was found from the bugreport https://bugs.launchpad.net/ubuntu/+source/libxml2/+bug/1032639

Simple gcc parse_tut.c won't work and will give undefined reference error.

After build is succesful,do this
$./a.out tut.c

keyword: 
		ramesh

This would be the output.The code is written for tut.xml and would not work for other documents.


