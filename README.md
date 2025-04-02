# Gwolf
A simple web server with the help of Go that utilizes wolfram kernel for compuatation


HTTP Request -> Go Web Server -> cgo call -> C Function (in libgowolf.so/dll/dylib)
                      ^                                          |
                      |                                          v
   HTTP Response <- Go Web Server <- cgo return <- C Function executes `wolframscript` -> Wolfram Kernel evaluates -> Prints result to stdout
