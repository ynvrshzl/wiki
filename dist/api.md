# API for database
When accessing this Wiki through a server, or external interfaces, the database provides a fast-access, static record of data for the wiki.

## Schema reference
The basic anatomy of a file's database
```json
[
    {
        // example
        path: "string",
        name: "string",
        folder: "string",
        outlinks: "string",
        date: [
            modified: "UTC",
            created: "UTC",
            edited: "UTC",
            accessed: "UTC",
        ],
        assets: [
            script: "main.js",
            css: "styles.css",
            html: "index.html",
        ],
        frontmatter: [],
    }
]
```