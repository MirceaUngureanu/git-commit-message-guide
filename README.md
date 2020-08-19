# 📝Write good commit messages

## Benefits
- Better understanding of the changes made
- Automation of logs
- Quicker navigation through git history (e.g. search for all commits with a type of docs)

## Rules for good messages
- Limit subject line and wrap the body lines at 72 characters
- Do not end subject with a period
- Use the imperative mood in the subject line (as if giving a command or instruction e.g. "update header content")
    - This follows the git built-in conventions
    - It should be able to complete this sentence: **This commit will _your subject line here_**
- Capitalise the subject line and each paragraph
- Use the body to explain what changes you have made and why you made them
- Separate the subject from the body with a blank line
- Do not think your code is self-explanatory
- Remove unnecessary punctuation marks
- Follow the commit convention defined by your team

## Commit message breakdown
Notes:<br />
`(scope)` - optional scope will be within parentheses<br />
`!` - optional breaking change flag<br />
`BREAKING CHANGE:` - optional breaking change footer

### With body
Only for non breaking changes.

Template:<br />
```
<type>[optional scope]: <description>
```
Examples:
```
feat(proxy): Add temporary redirect for About Page
```
```
feat: Add temporary redirect for About Page
```
### Commit message with body
If commit has breaking changes they need to be included in the breaking change footer.

Template:
```
<type>[optional scope][optional breaking change flag]: <description>

[optional body]

[optional footer(s)]
```
Example:
```
build!: upgrade gulp to version 4

More detailed explanation.

BREAKING CHANGE: Introduction of gulp.series and gulp.parallel.
Resolves: #123 
```

### Commit types

| Type       | Description                                                                  | Emoji* |
|------------|------------------------------------------------------------------------------|:------:|
| `feat`     | Add new feature for the user                                              |✨      |
| `fix`      | Fix a bug for the user                                                    |🐛      |
| `test`     | Add/Update tests                                                        |🔬      |
| `perf`     | Improve performance                                                        |🏎      |
| `refactor` | Refactor                                                                  |♻       |
| `build`    | Changes to the build system (updating/adding build tasks, etc)      |📦      |
| `ci`       | Changes to CI configuration files and scripts                                |⚙       |
| `docs`     | Documentation                                                                |📚      |
| `other`    | Changes not listed above and that are not production code changes (white-space, formatting, missing semi-colons, package manager changes etc) |🧰      |
| `revert`   | Revert commit/s                                                           |⏪      |
| `WIP`      | Work in progress**      |🚧      |

\* Using emojis to represent commit types is optional, keep in mind that sometimes they might not render well in all terminals.<br />
\** Only use WIP in exceptional cases and **never on the master branch**.

### Notes
- Removed the `style` type because it can cause confusion e.g. some might think it's to do with improving the readability of the code while some might think it's to do with UI style changes if working mainly in front-end 
- Replaced the `chore` type with `other` type which is less negative and more versatile

### References
I based this guide on [Angular commit convention](https://docs.google.com/document/d/1QrDFcIiPjSLDn3EL15IJygNPiHORgU1_OOAqWjiDU5Y/edit) and [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/), along with a dozen or so articles on the matter. I've tried to capture their essence without overloading this guide with too much detail.
