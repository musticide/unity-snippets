# Friendly Snippets

Snippets collection for a set of different programming languages.

The only goal is to have one community driven repository for all kinds of
snippets in all programming languages, this way you can have it all in one
place.

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

## Add snippets from a framework to a filetype.

> **Note**: This is handled by your snippet engine and has nothing to do with this snippets collection

There's extra snippets included in this repo but they are not added by default,
since it would be irrelevant for people not using those frameworks. See
[`snippets/frameworks`](https://github.com/musticide/unity-snippets/tree/main/snippets/frameworks)

For example: if you want to add rails snippets to ruby.

With LuaSnip:

```lua
require'luasnip'.filetype_extend("ruby", {"rails"})
```

With vim-vsnip:

```viml
let g:vsnip_filetypes.ruby = ['rails']
```

## Excluding snippets

> **Note**: This is handled by your snippet engine and has nothing to do with this snippets collection

With LuaSnip, see `help luasnip-loaders`

```lua
-- will exclude all javascript snippets
require("luasnip.loaders.from_vscode").load {
    exclude = { "javascript" },
}
```

- [vscode-standardjs-snippets](https://github.com/capaj/vscode-standardjs-snippets)
- [python-snippets](https://github.com/cstrap/python-snippets)
- [vs-snippets](https://github.com/kitagry/vs-snippets)
- [Wscats/html-snippets](https://github.com/Wscats/html-snippets)
- [Harry-Ross/vscode-c-snippets](https://github.com/Harry-Ross/vscode-c-snippets)
- [vscode-jekyll-snippets](https://github.com/edheltzel/vscode-jekyll-snippets)
- [vscode-fortran-support](https://github.com/krvajal/vscode-fortran-support)
- [vscode_cobol](https://github.com/spgennard/vscode_cobol)
- [VSCode-LaTeX-Snippets](https://github.com/JeffersonQin/VSCode-LaTeX-Snippets)
- [vscode-react-javascript-snippets](https://github.com/dsznajder/vscode-react-javascript-snippets)
- [honza/vim-snippets - Verilog](https://github.com/honza/vim-snippets/blob/master/snippets/verilog.snippets)
- [vscode-relm4-snippets](https://github.com/Relm4/vscode-relm4-snippets)
- And more...
