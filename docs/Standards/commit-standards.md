---
sidebar_position: 1
---

# Commit Standards


A commit combines changes into a logical unit. Adding a descriptive commit message can identify the code changes. Remember the following things when making a commit: 

- It's a good to make small commits. This makes changes easier to review and allows you to revert only the last changes if you discover a problem and also neatly explains exactly what changes were made and why. Split the commits into separate commits if it includes more than one logical changes or bug fix.
- Don't mix whitespace changes with functional code changes. It is hard to determine if the line has a functional change or only removes a whitespace, so functional changes may go unnoticed.
- Never commit incomplete code, its good to testing your code before committing.
- Write good commit messages. Use the imperative style in the subject line.
- Before making commits, ask yourself Why did I add this commit? and What changes does this commit make?

## Structure

- **subject**: a short description of the commit, maximum 50 characters long.
  -  subject **must not** be `['sentence-case', 'start-case', 'pascal-case', 'upper-case']`
- **body (optional)**: a longer description of the commit includes what, why and how, wrapped at 72 characters, separated from the subject line by a blank line

```bash
<type>: <description>

[optional body]

[optional footer]
```

### Type of commits

| Type          |   Usecase 
| ------------- | ---------------
| feat    | The new feature you're adding to a particular application
| fix     | Bug Fix
| style   | Feature and updates related to styling
| test    | Everything related to testing
| docs    | Changes made on the documentation, readme.md or markdown files
| chore   | Code maintenance such as modification or updating dependencies

Example of a commit message:
```bash
git commit -m "fix: commit Message"
```

## References

[Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)