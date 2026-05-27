# swift-clean-code

Clean Code skills for Swift / iOS projects based on Robert Martin's *Clean Code* and G. Ann Campbell's *Cognitive Complexity*.

## Skills

### Slash commands

| Command | What it does |
|---|---|
| `/swift-clean-names` | Review and fix naming: variables, functions, types, protocols |
| `/swift-clean-functions` | Audit function size, single responsibility, argument count, DRY |
| `/swift-clean-types` | Review class/struct/protocol design, SRP, dependency injection |
| `/swift-clean-errors` | Audit `throws`, optionals, `Result`, custom `Error` types |
| `/swift-clean-tests` | Check FIRST principles, AAA pattern, test naming, mocking |
| `/swift-clean-review` | Full Clean Code audit of a file or directory |
| `/swift-cognitive-complexity` | Score and reduce Cognitive Complexity: nesting, closures, control flow |

### Automatic (model-invoked)

`swift-clean-advisor` — activates when writing or editing Swift files. Applies Clean Code guidance without being asked.

## Installation

Install the whole bundle with one `npx` command:

```bash
npx skills add levabond/iOS-clean-code-skills --all
```

Or install only the skills you want:

```bash
npx skills add levabond/iOS-clean-code-skills --skill swift-clean-names --skill swift-clean-review
```

The CLI will ask which agents to register the skill with (Claude Code, Codex, Cursor, Gemini, ...) and whether to install per-project or globally.

If `npx` is missing, install Node (`brew install node`); if `brew` is missing too, [install Homebrew](https://brew.sh) first.

### Alternative install methods

**Claude Code** (installs the whole bundle directly):

```bash
/plugin install levabond/iOS-clean-code-skills
```

Or clone this repository and drop the skill folders wherever your agent expects them.

## Usage

```bash
# Review naming in a file
/swift-clean-names Sources/Auth/LoginViewModel.swift

# Audit function design
/swift-clean-functions Sources/Services/NetworkService.swift

# Full audit of a module
/swift-clean-review Sources/Features/Checkout/

# Review test quality
/swift-clean-tests Tests/UserServiceTests.swift

# Score and reduce cognitive complexity
/swift-cognitive-complexity Sources/Features/Checkout/CheckoutViewModel.swift
```

## Requirements

- Claude Code CLI (or another Agent Skills-compatible agent: Codex, Cursor, Gemini, ...)
- Xcode project (any architecture: MVC, MVVM, TCA, etc.)
