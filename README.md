# Rust Template

## Environment settings

### Install Rust

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

### Install VSCode Extensions

- crates: Rust package management
- Even Better TOML: TOML file support
- Better Comments: Optimized comment display
- Error Lens: Improved error prompts
- GitLens: Enhanced Git features
- Github Copilot: Code suggestions
- indent-rainbow: Indentation display optimization
- Prettier - Code formatter: Code formatting tool
- REST client: REST API debugging tool
- rust-analyzer：Rust language support
- Rust Test lens：Rust test support
- Rust Test Explorer：Rust test overview
- TODO Highlight：TODO highlighting
- vscode-icons：Icon optimization
- YAML：YAML file support

### Install cargo generate

cargo generate is a tool for generating project templates. It can use an existing GitHub repo as a template to generate a new project.

```bash
cargo install cargo-generate
```

The new project will use the `upupnoah/rust-template` template to generate basic code:：

```bash
cargo generate upupnoah/rust-template
```

### Install pre-commit

pre-commit is a code checking tool that can perform code checks before committing code.

```bash
pipx install pre-commit
```

After successful installation, run `pre-commit install`.

### Install cargo-deny

Cargo deny is a Cargo plugin that can be used to check the security of dependencies.

```bash
cargo install --locked cargo-deny
```

### Install typos

Typos is a spell checking tool.

```bash
cargo install typos-cli
```

### Install git-cliff

git cliff is a tool for generating changelogs.

```bash
cargo install git-cliff
```

### Install cargo nextest

cargo nextest is an enhanced testing tool for Rust.

```bash
cargo install cargo-nextest --locked
```

## Template Usage

1. cargo generate rust-noah/rust-template

2. Enter the directory, modify the cliff.toml file, change the URL after replace= to your own repository address (you need to create a repository first)

   1. Create an empty repository on GitHub (excluding README, .gitignore, and LICENSE).
   2. cd new-project-dir (Name of the new project)
   3. Execute the command in the empty project created in step 1 (git remote add ...)

3. pre-commit install

4. Change the package.name in the Cargo.toml file to the name of the new project.

Note:

- If git commit encounters problems, please delete `deny.toml` and then execute `cargo deny init`

  - Add the code below to licenses.

    ```toml
    unlicensed = "allow"
    allow = [
    "MIT",
    "Apache-2.0",
    "Unicode-DFS-2016",
    "MPL-2.0",
    "BSD-2-Clause",
    "BSD-3-Clause",
    "ISC",
    "CC0-1.0",
    ]
    ```
