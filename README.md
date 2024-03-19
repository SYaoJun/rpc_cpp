## tiny-rpc
- The repo origin from [buttonrpc_cpp14](https://github.com/button-chen/buttonrpc_cpp14)
## Compile
```c
mkdir build
cd build
cmake ..
make -j 8
```
## Dependencies
- zmq
```c
cd lib && git clone https://github.com/zeromq/libzmq.git && \
cd libzmq && mkdir build && cd build && cmake .. && make -j4 install && \
cd /lib && git clone https://github.com/zeromq/cppzmq.git && \
cd cppzmq && mkdir build && cd build && cmake .. && make -j4 install
cp /usr/local/lib/libzmq.so.5 /lib
```
## Attention
- On Ubuntu, We need the dynamic library libzmq.so.5.
- If you have installed, using your executable file links this lib.