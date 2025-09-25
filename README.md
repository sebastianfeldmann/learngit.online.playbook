# LearnGit.online Playbook

This repository contains the lessons for LearnGit.online, a platform teaching Git beyond the basics. Each lesson is stored in a **YAML format**, which makes it easy to read, edit, and contribute to. Lessons are structured as step-by-step scenarios with explanations, hints, and exercises, ready to be used at [leangit.online](http://learngit.online).

⚠️ **Work in Progress**  
This repository is still in early development. The lesson format, structure, and content may change at any time.

## Lesson Structure

Each lesson contains metadata and a list of steps. Key fields include:

- `title` – The lesson title.
- `description` – A short summary of the lesson.
- `category` – The lesson category (e.g., "basics", "advanced").
- `level` – Difficulty level (e.g., "beginner", "intermediate").
- `time` – Estimated duration of the lesson.
- `order` – Order in the sequence of lessons.
- `previous` / `next` – Links to the previous and next lesson.
- `steps` – The detailed steps of the lesson.

Each step can include:

- `id` – Step number or identifier.
- `title` – Step title.
- `description` – Short explanation of the step.
- `next` – Optional pointer to the next step.
- `allowedCommands` – List of allowed commands with expected outputs and hints.
    - `cmd` – The exact command the user can run.
    - `hint` – Optional hint to guide the user.
    - `valid` – Regex to validate input.
    - `output` – Optional simulated terminal output.

### Example Snippet

```yaml
title: "Git Commit Workflow"
description: "Learn the basics of staging and committing changes in Git."
category: "basics"
level: "beginner"
time: "10 minutes"
order: 1
previous: null
next: "git-push"
steps:
  - id: 1
    title: "Check repository status"
    description: "Start by checking the current status of your repository"
    allowedCommands:
      - cmd: "git status"
        valid: "^git\\s+status$"
        output:
          - text: |
              On branch main
              No commits yet
              Untracked files:
                README.md
                .gitignore
              nothing added to commit but untracked files present (use "git add" to track)
            hint: "This output shows we're on the <b>main</b> <i>branch</i> with no <i>commits</i> yet, and have <b>2 untracked files</b> that need to be added to version control."
        hint: "Shows the <strong>working tree status</strong> - which files are <i>tracked</i>, <i>untracked</i>, or <i>staged</i> for commit"
```

## License

All lesson content is licensed under [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)](https://creativecommons.org/licenses/by-nc-sa/4.0/).

You are free to share and adapt these lessons **for non-commercial purposes**, as long as you:

- Give appropriate credit to Sebastian Feldmann
- Include a link to the license
- Indicate if changes were made
- Distribute any derivative work under the same license

For example, a proper attribution could look like:

> "Contains LearnGit.online lessons by Sebastian Feldmann (https://learngit.online), licensed under CC BY-NC-SA 4.0."

