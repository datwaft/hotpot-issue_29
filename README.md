# Hotpot Issue [#29](https://github.com/rktjmp/hotpot.nvim/issues/29) Bug Reproduction

A reproduction of the hotpot issue [#29](https://github.com/rktjmp/hotpot.nvim/issues/29) using Docker.

This branch fixes the issue using this fix:
```sh
sed -i 's/(io\./(_G.io./g' config/fnl/lib/cljlib/init-macros.fnl
sed -i 's/(io\./(_G.io./g' config/fnl/lib/cljlib/init.fnl
```

## How to build and run

```sh
docker build -t nvim . && docker run -it nvim
```

After this just execute `nvim`.
