# Oni Haskell Language Server
The original intention was to create a LSP client for the Haskell language server, [HIE](https://github.com/haskell/haskell-ide-engine). It turns out it is possible to get the language server working, just by adding the following to your Oni configuration,

```javascript
  "language.haskell.languageServer.command": "hie",
  "language.haskell.languageServer.arguments": ["--lsp"],
  "language.haskell.languageServer.rootFiles": [".git"],
  "language.haskell.languageServer.configuration": {},
```

If you have installed HIE with the [`--compiler-tools`](https://github.com/haskell/haskell-ide-engine/blob/master/Makefile#L27), then the following will work for you,

```javascript
  "language.haskell.languageServer.command": "stack",
  "language.haskell.languageServer.arguments": ["exec", "--", "hie", "--lsp"],
  "language.haskell.languageServer.rootFiles": [".git"],
  "language.haskell.languageServer.configuration": {},
```
