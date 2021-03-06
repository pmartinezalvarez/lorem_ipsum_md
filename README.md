# Lorem Ipsum Markdown

Populates test sites with Markdown articles for testing the `glayu`, `jekyll` and `hugo` performance building static sites. 
 
Usage:

```console

$ lorem_ipsum_md  [-Cclp]

```

Generates a test site populated with "Lorem Ipsum" Markdown articles.


### Arguments

Argument | Description | Default Value
------------ | ------------- | ------------- |
`[-C, --categories]` | number of root categories | 10
`[-c, --children]` | number children per category/sub-category | 5
`[-l, --levels]` | site deep, number of subcategory levels (Ex: -l 3 produces categories like "1">"1_1">"1_1_1")| 3
`[-p, --platform]` | `glayu`, `jekyll` or `hugo` | `glayu`
`[-s, --size]` | number of articles per site | 10 000

### Examples

```console
$ lorem_ipsum_md  -categories 3 -children 2 -levels 3 -platform “glayu” -size 10000
```

Will generate a `glayu` site like:

```
.
└── source
   ├── 1
   |   ├── 1-1
   |   |   └── 1-1-1
   |   |   └── 1-1-2
   |   └── 1-2
   |        └── 1-2-1
   |        └── 1-2-2
   ├── 2
   |   ├── 2-1
   |   |   └── 2-1-1
   |   |   └── 2-1-2
   |   └── 2-2
   |        └── 2-2-1
   |        └── 2-2-2
   └── 3
       ├── 3-1
       |   └── 3-1-1
       |   └── 3-1-2
       └── 3-2
           └── 3-2-1
           └── 3-2-2
```

containing 1000 Markdown files uniformly dristributed throughout the site categories.

## License

This project is available under the MIT license.