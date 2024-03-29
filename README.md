# Unity Snippets

This is a fork of [friendly-snippets](https://github.com/rafamadriz/friendly-snippets)

## Install

Use your plugin manager of choice, e.g.

### With Lazy.nvim

```lua
{ "musticide/unity-snippets" }
```

> **Warning**: If you're using LuaSnip make sure to use
> `require("luasnip.loaders.from_vscode").lazy_load()`, and add
> `unity-snippets` as a dependency for LuaSnip, otherwise snippets might not
> be detected. If you don't use `lazy_load()` you might notice a slower
> startup-time
>
> ```lua
> {
>   "L3MON4D3/LuaSnip",
>   dependencies = { "musticide/unity-snippets" },
> }
> ```

### With Packer

```lua
use "musticide/unity-snippets"
```

### With vim-plug

```vim
Plug "musticide/unity-snippets"
```

### With coc.nvim

```vim
:CocInstall https://github.com/musticide/unity-snippets@main
```

## Usage

This collection of snippets should work with any snippet engine that supports
loading vscode snippets. Like for example:

- [vim-vsnip](https://github.com/hrsh7th/vim-vsnip)
- [LuaSnip](https://github.com/L3MON4D3/LuaSnip)
- [coc-snippets](https://github.com/neoclide/coc-snippets)

## Excluding snippets

> **Note**: This is handled by your snippet engine and has nothing to do with this snippets collection

With LuaSnip, see `help luasnip-loaders`

```lua
-- will exclude all javascript snippets
require("luasnip.loaders.from_vscode").load {
    exclude = { "javascript" },
}
```

# Credits
Unity snippets were taken from [VSCode Unity Code Snippets](https://github.com/kleber-swf/vscode-unity-code-snippets/blob/develop/snippets/snippets.json)
