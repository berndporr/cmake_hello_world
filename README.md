# cmake Hello World

Minimal cmake example to show how to create a library,
an executable and a test.

It provides a library with one function:
```
float mult5(float a);
```
which multiplies anything with 5!

Then a unit test tests this function if it really can do it.

And finally there a program using this amazing function!

## How to use

```
cmake .
make
make test
./helloworld
```

## Session output

```
$ cmake .
-- The CXX compiler identification is GNU 13.3.0
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Check for working CXX compiler: /usr/bin/c++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Configuring done (0.3s)
-- Generating done (0.0s)
-- Build files have been written to: /tmp/cmake_hello_world
$ make
[ 16%] Building CXX object CMakeFiles/mult5.dir/mult5.cpp.o
[ 33%] Linking CXX static library libmult5.a
[ 33%] Built target mult5
[ 50%] Building CXX object CMakeFiles/helloworld.dir/helloworld.cpp.o
[ 66%] Linking CXX executable helloworld
[ 66%] Built target helloworld
[ 83%] Building CXX object CMakeFiles/test_mult5.dir/test_mult5.cpp.o
[100%] Linking CXX executable test_mult5
[100%] Built target test_mult5
$ make test
Running tests...
Test project /tmp/cmake_hello_world
    Start 1: TestMult5
1/1 Test #1: TestMult5 ........................   Passed    0.00 sec

100% tests passed, 0 tests failed out of 1

Total Test time (real) =   0.01 sec
$ ./helloworld 
Hello World
6 mulipiled by 5 is: 30.000000
```
