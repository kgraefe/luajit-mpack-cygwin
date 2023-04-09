# luajit-mpack-cygwin

This a recipe to build and package [libmpack][1] for [Cygwin][2]. The recipe is
based on the [recipe in cascent's old neovim port][3].

Dependencies:
- [luajit{,-devel}][4]

To build the package install the dependencies and run the following command:
```sh
cygport luajit-mpack-cygwin.cygport download prepare compile install package
```

To install the package you can extract it into the root directory:
```sh
eval "$(cygport luajit-mpack.cygport vars PVR)"
tar -C / -xjvf luajit-mpack-$PVR.x86_64/dist/luajit-mpack/luajit-mpack-$PVR.tar.xz
```

[1]: https://github.com/libmpack/libmpack-lua
[2]: http://www.cygwin.com/
[3]: https://github.com/cascent/neovim-cygwin/blob/09277e3f76981189a2f15d1dbc2f5a4ab4b6c86f/luajit-mpack/luajit-mpack.cygport
[4]: https://github.com/kgraefe/luajit-cygwin
