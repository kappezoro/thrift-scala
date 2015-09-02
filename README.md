# thrift-scala

## How to use thrift)

- download bootstrap
-- [http://www.boost.org/](http://www.boost.org/)

```
tar xvzf boost_1_58_0.tar.gz
cd boost_1_58_0
./bootstrap.sh
sudo ./b2 threading=multi address-model=64 variant=release stage install
```

- download libevent
-- [http://libevent.org/](http://libevent.org/)

```
tar xvzf libevent-2.0.22-stable.tar.gz
cd libevent-2.0.22-stable
./configure --prefix=/usr/local
make
sudo make install
```

- download thrift
-- [https://thrift.apache.org/download](https://thrift.apache.org/download)

```
tar xvzf thrift-0.9.2.tar.gz
cd thrift-0.9.2
./configure --prefix=/usr/local/ --with-boost=/usr/local --with-libevent=/usr/local
```

* when you have error like 'Bison version 2.5 or higher must be installed on the system!'

```
brew install bison
bison -V

# if bison is < 2.5
which bison
# /usr/bin/bison
rm /usr/bin/bison

brew unlink bison
brew link bison --force
```
