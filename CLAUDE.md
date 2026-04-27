# Swift Clean Code Skills

Claude Code skills for iOS/Swift development based on **Clean Code** by Robert Martin.

## Installation

Copy the `.claude/` directory into your iOS project root:

```bash
cp -r /Users/levbondarenko/mobile/iOS-clean-code-skills/.claude /path/to/your/ios/project/
```

Or symlink (skills update automatically):

```bash
ln -s /Users/levbondarenko/mobile/iOS-clean-code-skills/.claude/skills /path/to/your/ios/project/.claude/skills
```

The skills activate automatically when you open Claude Code in your iOS project directory.

## Skills Reference

### User-Invoked Commands (slash commands)

| Command | Chapter | What it does |
|---|---|---|
| `/swift-clean-names` | Ch. 2 — Meaningful Names | Reviews and fixes all naming: variables, functions, types, protocols |
| `/swift-clean-functions` | Ch. 3 — Functions | Audits function size, SRP, argument count, side effects, DRY |
| `/swift-clean-types` | Ch. 6, 10 — Classes | Reviews class/struct/protocol design, SRP, cohesion, DI |
| `/swift-clean-errors` | Ch. 7 — Error Handling | Audits throws/optionals/Result usage, custom Error types |
| `/swift-clean-tests` | Ch. 9 — Unit Tests | Checks FIRST principles, AAA pattern, test naming, mocking |
| `/swift-clean-review` | All chapters | Full Clean Code audit of a file or entire directory |

### Model-Invoked (automatic)

| Skill | Activates when |
|---|---|
| `swift-clean-advisor` | Writing or editing Swift code — applies clean code guidance automatically |

## Usage Examples

```
# Review naming in a specific file
/swift-clean-names Sources/Features/Auth/LoginViewModel.swift

# Review function design
/swift-clean-functions Sources/Services/NetworkService.swift

# Full audit of a feature module
/swift-clean-review Sources/Features/Checkout/

# Review your test file
/swift-clean-tests Tests/UserServiceTests.swift
```

## Clean Code Principles Covered

Based on Robert Martin's *Clean Code* (2008):

1. **Ch. 2 — Meaningful Names**: intention-revealing names, no abbreviations, no noise words, consistent vocabulary
2. **Ch. 3 — Functions**: small, single responsibility, low argument count, no side effects, DRY
3. **Ch. 4 — Comments**: no noise comments, no commented-out code, explain WHY not WHAT
4. **Ch. 5 — Formatting**: vertical/horizontal organization, proximity rule
5. **Ch. 6 — Objects & Data Structures**: encapsulation, data/object anti-symmetry
6. **Ch. 7 — Error Handling**: throws over nil, meaningful Error types, no silent catches
7. **Ch. 9 — Unit Tests**: FIRST principles (Fast, Independent, Repeatable, Self-Validating, Timely)
8. **Ch. 10 — Classes**: SRP, high cohesion, open/closed principle
9. **Ch. 11 — Systems**: dependency injection, separate construction from use

### Swift-Specific Additions
- Prefer `struct` (value types) over `class`
- Protocol-Oriented Programming for dependency inversion
- `guard` for early exits instead of nested `if let`
- `async/await` over callbacks
- `throws` instead of optional returns for errors
- Swift Testing framework (`@Test`, `#expect`) alongside XCTest
