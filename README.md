# Markdown Post Generator CLI in Node.js

## Overview

This CLI allows generating a new Markdown post with frontmatter metadata for a blog or website. It prompts the user for a post title, then generates a filename and populates template frontmatter with title, date, author etc. The Markdown file is created in a `content/blog` directory.

## Usage

To use the CLI:

1. Clone the repo and install dependencies with `npm install`

2. Run `node index.cjs`

3. Enter a title when prompted

4. The Markdown file will be created in `content/blog`

## Code Overview

The main dependencies are:

- `readline` - for prompting user input
- `child_process` - to get Git author name 
- `fs` - for file system operations
- `path` - for resolving file paths

The key functions are:

- `textToSlug()` - generates a URL-friendly slug from a string 

- `rl.question()` - prompts user for title

- `rl.on('close')` - generates file name and frontmatter after title entered 

- `fs.writeFileSync()` - writes new Markdown file 

The frontmatter is populated from a template string with title, date, author etc.

Error handling is included for cases like existing file.

## Contributing

Pull requests are welcome to add features or fix bugs!

Some ideas:
// TODO
[]  - Support different frontmatter formats (YAML etc)
[]  - Add prompt for categories, tags
[]  - Allow passing filename on CLI instead of prompt
[]  - Wordpress to Markdown converter
[]  - Add tests
    