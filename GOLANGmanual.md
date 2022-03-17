GOLANGmanual
-> is description
= is result

======================
======================
======================
======================
======================
======================
Frameworks

Web - Gin, Fiber


======================

go build main.go
	-> compile program(main.go) into single binary 
	= main.exe

=====================
GOOS - 'goose'
======================
benefits of GO
Garbage collector-> dont have to manage memory 

======================
VSC set up

install go based on OS
install VSC GO extension in the VSC app 
the VSC GO extension depends on a set of other extensions, it say this or that
is missing, click install All
https://www.c-sharpcorner.com/article/how-to-setup-golang-with-vscode/

VERY HELPFUL ^^
======================
======================
======================
======================
======================
Gopher lang + other 
->|
++
Two ways to run main.go(a hello world application)

#1
go run main.go

#2 - compile source code into executable binary and name the object flag(-o dash+lowercase o)
go build main.go

go build -o helloWorld main.go

++
Create a module

go mod init <project name here>


++
Where is program entrypoint? main function 
++
fmt.Println vs fmt.Printf

Printf is like printf in C 

Println supports concatenation with strings and variables delimited by commas(,)
++ 
Type inference when you initialize a variable and assign it a value without a data type, 
go will infer the type 

e.g this will cause a bug b/c it initializes a variable but has no data type 
->| var userName
++
using %T in printf will print out the data type for the variable 
++
using := is only for variables and type inference. 
Can't be used when explicity assigning variable data types
++
Since seeds are constant, can use something like time to randomize things
++
Pointers are variables that point to the memory address of another variable
&varName for pointer reference of a variable

e.g
->|var userName string
->|fmt.Scan(&userName)
in this example, scan function gets a pointer as a parameter and assigns a value
to that memory address which is of the variable. 
++	
Arrays have fixed sizes at declaration, format = var <variable name> [<number of items size>]<data type>

e.g
var bookings = [50]string{"Nana", "Nicole", "Peter"}

e.g2

var bookings [50]string
bookings[0] = firstName + " " + lastName
bookings[1] = ""
++
Package log vs fmt

Log is safe from concurrent goroutines while fmt isnt 
Log can attach info automatically e.g time, date, file path,etc
++
log.Panic 
calls panic function

e.g
log.Panic("Panic message")


can also call recover function to recover the panic

if dont want to recover and program to exit right away, 
use log.Fatal
e.g
log.Fatal("Fatal message")
++
Print output to a file by creating the file, setting the output into the file, and then closing the file. After it sets the output back to standard. 
>>
file, _ := os.Create(name:"file.log")
log.SetOutput(file)
log.Println("Hello World!")
file.Close()
log.SetOutput(os.Stdout)
log.Println("Printing into standard out again")
>>
++
info, warning and error logger (FOR PRODUCTION)

>>
flags := log.LstdFlags | log.Lshortfile
infoLogger := log.New(os.Stdout, "INFO: ", flags)
warnLogger := log.New(os.Stdout, "WARN: ", flags)
errorLogger:= log.New(os.Stdout, "ERROR: ", flags)
infoLogger.Println("This is an info log")
warnLogger.Println("This is an warning log")
errorLogger.Println("This is an error log")

>>



======================
Learning slices 
->	its not just lists of strings, []bytes aka byte slices have to be learned
->	https://medium.com/@tyler_brewer2/bits-bytes-and-byte-slices-in-go-8a99012dcc8f
->	this link will explain bits and bytes. 
->	A byte is 8 bits. 
============
BYTES
============
A byte can also be a data type in go which is an unsigned 8 bit integer(0-255). Can also represent characters in a string.(SEE ASCII TABLE)
Zero value is 0 for a byte. 








====================
RESOURCES
====================
1.
2. Built-in functions - https://developpaper.com/built-in-functions-in-golang/
3. Built-in official golang doc - https://developpaper.com/built-in-functions-in-golang/
4.
====================
TOPICS WORTH GOOGLING FOR
=========================

1. What is the byte data type in golang?
2. Built-in functions in golang - SEE RESOURCE #2
3. 