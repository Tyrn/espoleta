# Espoleta

- [Rust Full Stack Workshop](https://bcnrust.github.io/devbcn-workshop/index.html)

## Shuttle

- [CLI](https://docs.shuttle.rs/getting-started/shuttle-commands)

```
cargo shuttle help
cargo shuttle project help
cargo shuttle project list
cargo shuttle project start
cargo shuttle project restart
cargo shuttle deploy --allow-dirty
...
```

## First start

- Create workspace (`espoleta/Cargo.toml`)

```
[workspace]
members = [
    "api/lib",
    "api/shuttle",
    "shared"
]
resolver = "2"
```

- Initialize the repository (`git init` in `espoleta`)

- Create `lib` crate: Library containing the code for the API.

```
cargo new api/lib --name api-lib --lib --vcs none
```

- Create `shuttle` crate: Executable for the shuttle project.

```
cargo shuttle init api/shuttle -t actix-web --name api-shuttle --force-name
```

- Create `shared` crate

```
cargo new shared  --lib
```
