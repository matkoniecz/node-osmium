# node-osmium

Flexible Javascript library for working with OpenStreetMap data.

Provides bindings to the [libosmium](https://github.com/osmcode/libosmium)
C++ library.

[![NPM](https://nodei.co/npm/osmium.png?downloads=true&downloadRank=true)](https://www.npmjs.com/package/osmium)
[![Build Status](https://api.travis-ci.org/osmcode/node-osmium.svg)](https://travis-ci.org/osmcode/node-osmium)
[![CI](https://github.com/osmcode/node-osmium/workflows/CI/badge.svg?branch=master)](https://github.com/osmcode/node-osmium/actions)
[![Coverage Status](https://coveralls.io/repos/osmcode/node-osmium/badge.svg?branch=coverage)](https://coveralls.io/r/osmcode/node-osmium?branch=coverage)
[![Dependencies](https://david-dm.org/osmcode/node-osmium.svg)](https://david-dm.org/osmcode/node-osmium)


## Should you use node-osmium?

If you want top performance use libosmium directly in C++. These node-osmium
bindings, due to the expense of passing objects from C++ to Javascript, are
much slower than working in C++ directly. Consider `node-osmium` only for small
extracts and prototyping. For large extracts or planet processing we recommend
leveraging the [libosmium C++ API](https://github.com/osmcode/libosmium)
instead of using node-osmium.


## Is node-osmium actively developed?

@springmeyer and @joto are not actively maintaining node-osmium or adding
features. We will consider pull requests adding features only when they come
with very solid tests, add very clear value to the bindings, and seem easy to
maintain.


## Depends

 - Node.js v8.x, v10.x, v12.x, v14.x
 - Mocha (http://mochajs.org/, for tests)
 - Compiler that supports `-std=c++11` (>= clang++ 3.6 || >= g++ 4.8)
 - [libosmium](https://github.com/osmcode/libosmium) >= 2.10.3
   (Debian/Ubuntu: libosmium2-dev)
 - [protozero](https://github.com/mapbox/protozero) >= 1.5.1
   (Debian/Ubuntu: libprotozero-dev)
 - [Utfcpp](http://utfcpp.sourceforge.net/)
   Only needed for libosmium version < 2.14.1, included in the libosmium
   repository and might or might not have been installed with it. See the
   libosmium README.
   (Debian/Ubuntu: libutfcpp-dev)
 - [Boost](http://www.boost.org/) >= 1.55 with development headers
   (Debian/Ubuntu: libboost-dev)
 - [zlib](http://www.zlib.net/)
   (Debian/Ubuntu: zlib1g-dev)
 - [expat](http://expat.sourceforge.net/)
   Debian/Ubuntu: libexpat1-dev
 - [sparsehash](https://github.com/sparsehash/sparsehash)
   Debian/Ubuntu: libsparsehash-dev

If you have problems compiling, install the dependencies for libosmium first
and make sure it works. Then you should be able to get node-osmium to compile.


## Installing

By default, binaries are provided and no external dependencies or compile is
needed.

Just do:

```shell
npm install osmium
```

We currently provide binaries for 64 bit OS X and 64 bit Linux. Running `npm
install` on other platforms will fall back to a source compile (see
`Developing` below for build details).


## Usage

See [the tutorial](doc/tutorial.md) for an introduction. There are some demo
applications in the 'demo' directory. See the [README.md](demo/README.md)
there. You can also have a look at the tests in the `test` directory.


## Developing

If you wish to develop on `node-osmium` you can check out the code and then
build like:

```shell
git clone https://github.com/osmcode/node-osmium.git
cd node-osmium
make
```

Use `make debug` to build with debug information. Use `make coverage` to build
with code coverage.

Use `make VERBOSE=1` to output compiler calls used etc.


## Testing

    npm install mocha
    make test


## License

node-osmium is available under the Boost Software License. See LICENSE.txt for
details.


## Contact

Please open bug reports on https://github.com/osmcode/node-osmium/issues. You
can ask questions on the
[OSM developer mailing list](https://lists.openstreetmap.org/listinfo/dev)
or on [OFTC net IRC channel #osm-dev](https://wiki.openstreetmap.org/wiki/Irc).


## Authors

 - Dane Springmeyer (dane@mapbox.com)
 - Jochen Topf (jochen@topf.org)

