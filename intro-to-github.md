# GitHub

## What is GitHub?

GitHub is a platform that hosts Git repositories. It provides a lot of features on top of Git, such as:

- [**Actions**](#actions): Automate testing your code before merging it onto `main` and deploying it to production.
- [**Issues**](#issues): Track bugs, enhancements and feature requests.
- [**Projects**](#projects): Organize your work through tasks and milestones.
- [**Discussions**](#discussions): Discuss, ask questions, and share information.
- [**Wiki**](#wiki): Create a wiki for your repository.
- [**Pages**](#pages): Host a website directly from your repository.

## GitHub features

### Actions

GitHub Actions allows you to automate executing of your software development workflows right in your repository. You can use it to build, test and deploy your code to production.

To create a GitHub Action, you need to create a `.github/workflows` directory in your repository and add a `.yml` file with your workflow configuration. This process is called "Continuous Integration" (CI) and "Continuous Deployment" (CD).

### Issues

Issues are used to track bugs, enhancements and feature requests. They can be assigned to a user, labeled and (optionally) have a milestone. You can also reference issues in your [commits](./intro-to-git.md#staging-and-committing) and [pull requests](./intro-to-git.md#pull-requests) using `#` followed by the issue number to mark it as related to the issue:

```sh
git commit -m "Fix #123 bug with the login form"
```

### Projects

Projects help you organize your work through tasks and milestones. You can create a project board for specific feature, track its progress and assign tasks to team members.

### Discussions

Discussions allow you to discuss, ask questions, and share information with other members of your repository.

### Wiki

GitHub Wiki allows you to create a wiki for your repository written in [Markdown](#markdown). You can use it to document your project and write the project's roadmap.

**Pro tip**: GitHub Wikis are also repositories, so you can clone them and work on them locally with `git clone`!

### Pages

GitHub Pages allows you to host a website directly from your repository. You can use it to host your documentation, portfolio, blog, or any other static website.

## Markdown

Markdown is a lightweight, human-readable markup language (conversely to HTML) with plain-text-formatting syntax. In the context of GitHub, it is used to write documentation, issues and pull requests.

You can use Markdown to format text, add images, create lists, and more.

### Markdown basics

Markdown has two types of syntax:

### Inline

Inline syntax is used to **format text within a paragraph**.

| Formatting     | Syntax                          | Output                                      |
|----------------|---------------------------------|---------------------------------------------|
| Bold           | `**text**` or `__text__`        | **text**                                    |
| Italic         | `*text*` or `_text_`            | *text*                                      |
| Strikethrough  | `~~text~~`                      | ~~text~~                                    |
| Code           | \`code\`                        | `code`                                      |
| Math           | `$math^2$`                      | $math^2$ (see [LaTeX](https://en.wikibooks.org/wiki/LaTeX/Mathematics)) |
| Links          | `[text](url)`                   | [GitHub](https://github.com)                |
| Images         | `![alt text](url)`              | ![GitHub logo](https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png) |

### Block

Block syntax is used to create **self-contained elements** like headers, lists and blockquotes. All block elements are separated by a:

- Blank line around them.
- Space after the character that starts them.

| Formatting      | Syntax                            |
|-----------------|-----------------------------------|
| Paragraphs      | Text separated by a blank line    |
| Headers         | `#` * the level (`#` to `######`) |
| Bullet lists    | `*` or `-` per item               |
| Numbered lists  | `1.`, `2.`, etc. per item         |
| Blockquotes     | `>` at the start of a paragraph   |
| Code blocks     | ` ``` ` before and after the code |
| Horizontal rule | `---` or `***` or `___`           |

In code blocks, you can specify the language to get syntax highlighting (e.g. ````python`):

```python
def hello_world():
    print("Hello, world!")
```

Last but not least, you can create diagrams using [Mermaid](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-diagrams#creating-mermaid-diagrams):

```mermaid
graph TD;  # TD = top-down, LR = left-right, RL = right-left, BT = bottom-top
  A-->B;
  A-->C;
  B-->D;
  C-->D;
```

### Markdown in GitHub

GitHub uses a specific flavor of Markdown called ["GitHub Flavored Markdown" (GFM)](https://github.github.com/gfm/). It adds a few nice extra features to the standard Markdown.

#### Task lists

You can create task lists by prefixing list items with `- [ ]` or `- [x]`:

- [x] Finish my changes
- [ ] Push my commits to GitHub
- [ ] Open a pull request

#### Tables

You can create tables by using `|` to separate columns and `-` to separate the header from the content:

```markdown
| First Header  | Second Header |
|---------------|---------------|
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |
```

You get:

| First Header  | Second Header |
|---------------|---------------|
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |

To align the content, you can use `:---` to align left, `---:` to align right, and `:---:` to center. The number of `-`s doesn't matter.

#### Alerts

You can create alerts by using `> [!ALERT-NAME]` at the start of a paragraph:

```markdown
> [!NOTE]
> This is a note.

> [!TIP]
> This is a tip.

> [!WARNING]
> This is a warning.

> [!CAUTION]
> This is a caution.

> [!IMPORTANT]
> This is important.
```

You get:

<!-- markdownlint-disable MD028 -->

> [!NOTE]
> This is a note.

> [!TIP]
> This is a tip.

> [!WARNING]
> This is a warning.

> [!CAUTION]
> This is a caution.

> [!IMPORTANT]
> This is important.

<!-- markdownlint-enable MD028 -->
