## Overview

It's a test project of [googletest](https://github.com/google/googletest).

Nothing but test the API and features.

## How to Build and Run

- Builld googletest

      $ cd googletest-release-1.8.0
      $ mkdir build && cd build
      $ mkdir install && cmake -DCMAKE_INSTALL_PREFIX=${PWD}/install ..
      $ make -j`nproc` && make install
   
  See `deps/gtest`, it's pre-built version.

- Build the test code
        
      $ cd try-googletest
      $ mkdir build && cd build
      $ cmake ..
      $ make -j`nproc`
        
- Run 

      $ cd try-googletest
      $ ./build/sample1_unittest