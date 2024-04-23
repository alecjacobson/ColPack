_See [original README.md](https://github.com/CSCsw/ColPack/blob/master/README.md)_

This fork attempts to fix issues with openmp on macos.

First install openmp using homebrew

    brew install libomp

Then 

    mkdir build/cmake/build
    cd build/cmake/build
    cmake .. -DCMAKE_INSTALL_PREFIX:PATH=../ -DENABLE_OPENMP=ON -DCMAKE_PREFIX_PATH="/opt/homebrew/opt/libomp"
    make -j8
    make install
