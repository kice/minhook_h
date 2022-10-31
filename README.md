# MinHook single header

Since I need to create a lot of project that will use MinHook, 
so I think make it single header will make my life easier.

## What did you change?

1. Merge all files into single header
2. Cleanup all `#define` marco
3. Change name of all global variables and type names
4. Make all "non-public" functions `static`
5. Remove `pstdint.h`, use `<stdint.h>` instead.
6. Only "public" functions are have `extern "C"`, other functions dose not.

## How to use

Before including, 

```c
#define MIN_HOOK_IMPLEMENTATION
```

in the file that you want to have the implementation.

If you need to use `<Windows.h>`, 
define marcos like "WIN32_LEAN_AND_MEAN" **BEFORE** include this file

```c
#define WIN32_LEAN_AND_MEAN
```

## Can I make a DLL using this?

Yes, you can. ~~but why?~~

You need to copy [MinHook.def](https://github.com/TsudaKageyu/minhook/blob/master/dll_resources/MinHook.def) from original repo, and it to the project. 
