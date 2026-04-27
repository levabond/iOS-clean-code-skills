# swift-clean-code

Clean Code skills for Swift / iOS projects based on Robert Martin's *Clean Code*.

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

### Automatic (model-invoked)

`swift-clean-advisor` — activates when writing or editing Swift files. Applies Clean Code guidance without being asked.

## Installation

Copy `.claude/` into your iOS project root:

```bash
cp -r .claude /path/to/your/ios/project/
```

Then open Claude Code in that project — skills are available immediately.

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
```

## Requirements

- Claude Code CLI
- Xcode project (any architecture: MVC, MVVM, TCA, etc.)
