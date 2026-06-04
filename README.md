# pluma

> Multi-canvas authoring — a *bundle of bodies* over one material — plus a reactive notebook, on [Llimphi](https://gitea.gioser.net/sergio/llimphi).

`pluma` (Spanish: *feather/pen*) is a writing tool where a document is a **bundle of `Cuerpo`s** (canvases: language, tone, audience, summary, version) over the same material, aligned paragraph-by-paragraph. Transformations (translate / tone / summarize / rewrite / custom-Rhai) derive a child body from a mother; if the mother changes, the child goes stale and the UI offers to regenerate. It also ships a **reactive notebook**: a DAG of cells run in topological order with swappable kernels (LLM, dominium, cosmos, python, wasm).

## Run
```sh
cargo run --release -p pluma-editor-llimphi --example multilienzo_demo
```

## How dependencies work
Front-door repo: only `pluma-*` crates here (including the `pluma-llm` backend façade and notebook kernels). Llimphi and shared foundations are git-dependencies of the [`gioser`](https://gitea.gioser.net/sergio/gioser) monorepo.

## License
MIT. Builds on [Llimphi](https://gitea.gioser.net/sergio/llimphi) + the [gioser](https://gitea.gioser.net/sergio/gioser) suite.
