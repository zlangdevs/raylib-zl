# Raylib bindings for ZLang
Bindings are at very early stage.

`raylib.zl` is a main file to include.

## Demo
In `demo/` directory there are examples of using raylib in ZLang.

## How to use 
1. Put `use raylib` in the beggining of `.zl` file
2. Check [Raylib Cheatsheet](https://www.raylib.com/cheatsheet/cheatsheet.html) - function names in ZLang wrapper remains the same.
3. To compile the program include path to `raylib.zl` and link the static version of raylib: `-link libraylib.a` (change the path to raylib binary if needed)
4. add raylib's dependencies: `-lGL -lm -lpthread -ldl -lrt -lX11`

### Example: 
```bash
./zlang demo/arrow_ball.zl raylib.zl -link bin/libraylib.a -lGL -lm -lpthread -ldl -lrt -lX11 && ./output
```

## ABI Problems
ZLang doesn't support C ABI yet, so, there are problems with some structs from Raylib. For example, to pass argument of type Color, you should to use Color.pack() method. These aspects are shown in examples 