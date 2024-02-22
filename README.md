<p align="center">
  <h1 align="center">
    Your Notes
  </h1>
  <p align="center"><i>Your Description Here</i></p>
</p>

<p align="center"> 
    <a href="https://opensource.org/licenses/MIT" target="_blank">
        <img alt="License: MIT" src="https://img.shields.io/badge/license-MIT-6495ED.svg">
    </a>
    <!-- update the repo link below in img src! -->
    <a href="./.github/workflows/deploy-book.yml" target="_blank">
        <img alt="Workflow: Book Deployment" src="https://github.com/erhant/mdbook-template/actions/workflows/deploy-book.yml/badge.svg?branch=main">
    </a>
</p>

## Setup

We use [mdBook](https://github.com/rust-lang/mdBook) along with several plugins:

- [mdbook-katex](https://github.com/lzanini/mdbook-katex) for math displays.
- [mdbook-mermaid](https://github.com/badboy/mdbook-mermaid) for MermaidJS renders.
- [mdbook-toc](https://github.com/badboy/mdbook-toc) for table of contents.
- [css](./utilities/custom.css) is a custom CSS to align Mermaid outputs to center.

You need to have Rust installed for all of this.

## Usage

After setup is complete, you can use the following commands:

```sh
# serve
mdbook serve --open

# build
mdbook build
```

> [!TIP]
>
> You can also use these scripts via `make`.

The book content is written under the [content](./content/) folder; this allows for some code examples to be written under `src` and some tests under `tests` if need be.

### Deploy to Vercel

The provided [workflow](./.github/workflows/deploy-book.yml) deploys to Vercel on workflow dispatch (though feel free to make it trigger on each push). For the workflow, you need to provide some repository secrets to the GitHub repo:

- `VERCEL_TOKEN`: Vercel token for the project
- `VERCEL_ORG_ID`: Vercel organization ID, or your user ID
- `VERCEL_PROJECT_ID`: Vercel project ID

## Examples

- [circom.erhant.me](https://circom.erhant.me/)
- [crypto.erhant.me](https://crypto.erhant.me/)
- [math.erhant.me](https://math.erhant.me/)

## License

This repository is MIT licensed, see [LICENSE](./LICENSE).
