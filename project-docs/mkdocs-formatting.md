# MkDocs Formatting

## Links

### Links to files
  - In the same dir: `[Alt text](filename.md)`
  
For example, from `vintage-reel-service-guides/project-docs/mkdocs-formatting` to `vintage-reel-service-guides/project-docs/photo-standards` is `[Photo Standards](photo-standards.md)`

  - In a dir one level up: [Alt text](../dir/filename.md)
For example, from `vintage-reel-service-guides/project-docs/mkdocs-formatting` to `vintage-reel-service-guides/docs/references` is `[References](../docs/references.md)`
Each ../ goes up one level in the dir structure, so two levels up would be ../../

  - If the target is in a different dir/subdir off the root, add the path: (../img/dir/dir/filename.md)

### Links to images

`![Alt text](path.jpg)`

For example, ![Penn 720--Front Left](../../img/penn/720/penn-720-front-left.jpg)
