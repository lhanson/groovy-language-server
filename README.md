# Groovy Language Server

**Fork note**: This was forked to tweak the dependencies slightly to work around a bug in `gradle2nix` where BOM dependencies were not being resolved: [https://github.com/tadfisher/gradle2nix/issues/33](https://github.com/tadfisher/gradle2nix/issues/33).

Generating the nix files also requires using a fork of `gradle2nix` due to mismatched SHA256 hashes:
`nix run github:numtide/gradle2nix -- -g 7.3`.

A [language server](https://microsoft.github.io/language-server-protocol/) for [Groovy](http://groovy-lang.org/).

The following language server protocol requests are currently supported:

- completion
- definition
- documentSymbol
- hover
- references
- rename
- signatureHelp
- symbol
- typeDefinition

## Build

To build from the command line, run the following command:

```sh
./gradlew build
```

This will create _build/libs/groovy-language-server-all.jar_.

## Run

To run the language server, use the following command:

```sh
java -jar groovy-language-server-all.jar
```

Language server protocol messages are passed using standard I/O.
