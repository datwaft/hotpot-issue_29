# Hotpot Issue [#29](https://github.com/rktjmp/hotpot.nvim/issues/29) Bug Reproduction

A reproduction of the hotpot issue [#29](https://github.com/rktjmp/hotpot.nvim/issues/29) using Docker.

This branch fixes the issue using this fix:

```lua
require("hotpot").setup({
    compiler = {
        macros = {env = "_COMPILER", compilerEnv = _G, allowedGlobals = false}
    }
})
```

## How to build and run

```sh
docker build -t nvim . && docker run -it nvim
```

After this just execute `nvim`.
