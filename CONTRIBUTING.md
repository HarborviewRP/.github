  # Harborview Contribution Guidelines

The following is a set of guidelines for contributing to plugins used on the Harborview, which are hosted in the [Harborview Organization](https://github.com/HarborviewRP) on GitHub. These are mostly guidelines, not rules. Use your best judgment, and feel free to propose changes to this document in a pull request.

#### Table Of Contents

[Code of Conduct](#code-of-conduct)

[What should I know before I get started?](#what-should-i-know-before-i-get-started)

[How Can I Contribute?](#how-can-i-contribute)

-   [Reporting Bugs](#reporting-bugs)
-   [Suggesting Enhancements](#suggesting-enhancements)
-   [Your First Code Contribution](#your-first-code-contribution)
-   [Pull Requests](#pull-requests)

[Styleguides](#styleguides)

-   [Git Commit Messages](#git-commit-messages)
-   [Documentation Styleguide](#documentation-styleguide)

[Additional Notes](#additional-notes)

-   [Issue and Pull Request Labels](#issue-and-pull-request-labels)

## What should I know before I get started?

### APIs We Utilise

### MySQL and PostgreSQL

We use MySQL/MariaDB for our SQL Databases

-   [MySQL](https://dev.mysql.com/doc/)

### Suggesting Enhancements

This section guides you through submitting an enhancement suggestion for Harborview plugins, including completely new features and minor improvements to existing functionality. Following these guidelines helps maintainers and the community understand your suggestion :pencil: and find related suggestions :mag_right:.

Before creating enhancement suggestions, please check [this list](#before-submitting-an-enhancement-suggestion) as you might find out that you don't need to create one. When you are creating an enhancement suggestion, please [include as many details as possible](#how-do-i-submit-a-good-enhancement-suggestion). Fill in [the template](https://github.com/HarborviewRP/.github/ISSUE_TEMPLATE/feature_request.md), including the steps that you imagine you would take if the feature you're requesting existed.

#### Before Submitting An Enhancement Suggestion

-   **Determine which repository the enhancement should be suggested in.**
-   **Perform a [cursory search](https://github.com/search?q=+is%3Aissue+user%3ATBDSRP)** to see if the enhancement has already been suggested. If it has, add a comment to the existing issue instead of opening a new one.

#### How Do I Submit A (Good) Enhancement Suggestion?

Enhancement suggestions are tracked as [GitHub issues](https://guides.github.com/features/issues/). After you've determined which repository your enhancement suggestion is related to, create an issue on that repository and provide the following information:

-   **Use a clear and descriptive title** for the issue to identify the suggestion.
-   **Provide a step-by-step description of the suggested enhancement** in as many details as possible.
-   **Provide specific examples to demonstrate the steps**. Include copy/pasteable snippets which you use in those examples, as [Markdown code blocks](https://help.github.com/articles/markdown-basics/#multiple-lines).
-   **Describe the current behavior** and **explain which behavior you expected to see instead** and why.
-   **Include screenshots and animated GIFs** which help you demonstrate the steps or point out what the suggestion is related to. You can use [this tool](https://www.cockos.com/licecap/) to record GIFs on macOS and Windows, and [this tool](https://github.com/colinkeenan/silentcast) or [this tool](https://github.com/GNOME/byzanz) on Linux.
-   **Explain why this enhancement would be useful**.
-   **List some other plugins where this enhancement exists.**

### Branch Naming Convention

To help everyone understand what you are currently working on in your branch, we ask you to abide by the following branch naming convention:

-   For a feature you are adding, use: `feat/<your username>/<short feature name>` e.g. `feat/zachery/mail`.
-   For a bugfix, use: `bugfix/<your username>/<short bug name>` e.g. `bugfix/zachery/overflow`.
-   For a critical patch to master, use `hotfix/master`.

### Pull Requests

The process described here has several goals:

-   Maintain the quality of Harborview's resources
-   Fix problems that are important to players
-   Engage the community in working toward the best possible gameplay experience

Please follow these steps to have your contribution considered by the maintainers:

1. Follow all instructions in [the template](https://github.com/HarborviewRP/.github/blob/main/ISSUE_TEMPLATE/feature_request.md)
2. Follow the [styleguides](#styleguides)
3. After you submit your pull request, verify that all [status checks](https://help.github.com/articles/about-status-checks/) are passing <details><summary>What if the status checks are failing?</summary>If a status check is failing, and you believe that the failure is unrelated to your change, please leave a comment on the pull request explaining why you believe the failure is unrelated. A maintainer will re-run the status check for you. If we conclude that the failure was a false positive, then we will open an issue to track that problem with our status check suite.</details>

While the prerequisites above must be satisfied prior to having your pull request reviewed, the reviewer(s) may ask you to complete additional design work, tests, or other changes before your pull request can be ultimately accepted.

## Styleguides

### Git Commit Messages

-   Be descriptive ("feat: Add x, y, and z" not "added stuff")
-   Prefix all commits with `feat:`, `fix:`, `refactor:`, or `misc:` ("fix: Move cursor to..." not "Move cursor to...")
-   Use the present tense ("feat: Add x, y, and z" not "Added x, y, and z")
-   Use the imperative mood ("fix: Move cursor to..." not "fix: Moves cursor to...")
-   Limit the first line to 72 characters or less
-   Reference issues and pull requests liberally after the first line

### General Code Styleguide

-   Use guard clauses where possible

    ```lua
      -- Use this
      if not condition then return end

      -- Don't use this
      if condition then
        -- code
      end
    ```
-   Refrain from using if else chains if possible

    ```lua
      -- Use this
      local var = math.max(0, math.min(input, 100))
      
      -- Don't use this
      local var
      if input < 0 then
          var = 0
      elseif input > 100 then
          var = 100
      else
          var = input
      end
    ```
- Use consisent quotes. (i.e. use only `'` or only `"` in your projects.
- Follow a consistent naming convention (e.g., camelCase, snake_case) throughout your codebase to enhance readability. For the purpose of our scripts, please use snake_case.

- Aim to write code that is self-explanatory and easy to understand. Use meaningful variable and function names, avoid ambiguous abbreviations, and include comments when necessary to clarify complex logic or intentions.

- Divide complex tasks into smaller, manageable functions. This promotes code reusability, enhances readability, and allows for easier debugging and testing.

- Identify repetitive code patterns and refactor them into reusable functions or modules. Duplicated code increases maintenance effort, introduces the risk of inconsistencies, and makes code harder to understand.

-  Aim to keep functions and methods focused on a single task. This promotes code clarity and makes it easier to understand, test, and maintain. If a function becomes too long or complex, consider breaking it down into smaller functions.

### Documentation Styleguide
-   Use [Markdown](https://daringfireball.net/projects/markdown) for directory-level documentation.
