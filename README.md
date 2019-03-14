CuPy-cuDF-cuML
==============

Use CuPy ndarray with cuDF/cuML functions

```
git clone https://github.com/rapidsai/cudf
git submodule update --init --recursive

conda install -c nvidia nvstrings

cd cudf
mkdir -p cpp/build && cd cpp/build
BOOST_INCLUDEDIR=$HOME/.linuxbrew/include cmake ../ -DCMAKE_INSTALL_PREFIX=$HOME
LIBRARY_PATH=$(pyenv prefix)/lib:$LD_LIBRARY_PATH CPATH=$(pyenv prefix)/include:$CPATH make -j install
make python_cffi
make install_python
```
