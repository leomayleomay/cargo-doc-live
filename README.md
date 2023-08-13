# cargo-doc-live

Flake module to provide live server version of `cargo doc`

## Getting Started

Import this along with the process-compose-flake module,

```nix
imports = [
  inputs.process-compose-flake.flakeModule
  inputs.cargo-doc-live.flakeModule
];
```

Add the following to the `packages` of your devShell

```nix
packages = [
  config.process-compose.cargo-doc-live.outputs.package
];
```

This will make the `cargo-doc-live` command available in your shell.

