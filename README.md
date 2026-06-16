# pluma

> Multi-canvas authoring — a *bundle of bodies* over one material — plus a reactive notebook, on [Llimphi](https://github.com/tawasuyu/llimphi).

`pluma` (Spanish: *feather/pen*) is a writing tool where a document is a **bundle of `Cuerpo`s** (canvases: language, tone, audience, summary, version) over the same material, aligned paragraph-by-paragraph. Transformations (translate / tone / summarize / rewrite / custom-Rhai) derive a child body from a mother; if the mother changes, the child goes stale and the UI offers to regenerate. It also ships a **reactive notebook**: a DAG of cells run in topological order with swappable kernels (LLM, dominium, cosmos, python, wasm).

<p align="center">
  <img src="docs/pluma_showreel.gif" alt="pluma showreel — the same document as three parallel bodies (Spanish, Quechua, English) aligned paragraph-by-paragraph with alignment threads" width="900">
  <br>
  <sub>one document as a bundle of parallel bodies — Spanish · Quechua · English, aligned paragraph-by-paragraph</sub>
</p>

## Run
```sh
cargo run --release -p pluma-editor-llimphi --example multilienzo_demo
```

## How dependencies work
Front-door repo: only `pluma-*` crates here (including the `pluma-llm` backend façade and notebook kernels). Llimphi and shared foundations are git-dependencies of the [`tawasuyu`](https://github.com/tawasuyu/tawasuyu) monorepo.

## License
MIT. Builds on [Llimphi](https://github.com/tawasuyu/llimphi) + the [tawasuyu](https://github.com/tawasuyu/tawasuyu) suite.
