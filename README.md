# Raylib bindings for ZLang
Bindings are at very early stage. Most functions and structs are not supported yet.

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
### Screenshots
<img width="825" height="466" alt="image" src="https://github.com/user-attachments/assets/00ba60a6-3eba-4bc6-8d67-4b50fa320da7" />
<img width="812" height="466" alt="image" src="https://github.com/user-attachments/assets/583ddd97-faaf-44b9-83b3-bf8b951b505f" />
