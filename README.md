# Commit hook to render PlantUML files

Minimal hook that renders puml to images whenever they're edited, uses a
Docker container so there's no dependencies. Use the title of your plantuml
document to control the file name, control the output with the usual command
line arguments: <https://plantuml.com/command-line>

For example, to generate in svg without the metadata you'd want something like
this (it should probably be the default really)

```yaml
-   repo: https://github.com/bitplane/plantuml-docker-pre-commit-hook
    rev: v0.0.3
    hooks:
    -   id: plantuml-docker
        args: [-tsvg, -nometadata]
```
