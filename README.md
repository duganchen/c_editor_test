# Editor Testing Playground

A C project intended to be an a playground for testing editors. I got tired of constantly putting these together and
decided to version one.

It is *just* complicated enough to play with;

* jumps between declarations and definitions (across files)
* debugging and breakpoints
* rename-refactorings

A Cmake file and a Makefile are included.

For CMake, you initialize neovim's LSP support with:

    mkdir build
    cd build
    cmake .. -DCMAKE_EXPORT_COMPILE_COMMANDS=ON
    cd ..
    ln -s build/compile_commands.json

The Makefile is there because vim's makeprg is designed for one.
