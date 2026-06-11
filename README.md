# terminal-portfolio

A single-file personal portfolio styled as an interactive terminal. Visitors type commands (`help`, `about`, `projects`, `contact`) and get formatted output. Replace the data, ship.

**Live demo:** https://0xelitesystem.github.io/terminal-portfolio/

## Why

Standard portfolios are hard to make interesting because everyone has one. A terminal is a different surface: visitors who get the joke explore for fun, visitors who don't can still type `help` and find what they need.

## Use it

Open `index.html` in any browser, or visit the hosted version at `https://0xelitesystem.github.io/terminal-portfolio/` once Pages is enabled.

Type a command and press Enter. Try `help` first.

## Customize

All data lives in a `CONFIG` object at the top of the script block. Edit these:

- `handle`, your username (shows in the title bar)
- `prompt`, the shell prompt (default: `guest@portfolio:~$`)
- `banner`, ASCII art shown on load (use any ASCII generator or none)
- `welcomeText`, first line under the banner
- `about`, array of bio lines
- `skills`, object of categories to skill lists
- `projects`, array of `{name, desc, url}` for each project
- `contact`, array of `{label, value, url}` for each contact method
- `social`, array of "label: url" strings

To add a new command, add a key to the `COMMANDS` object. Commands are functions that return HTML or null (null suppresses output).

## Built-in commands

`help`, `about`, `skills`, `projects`, `contact`, `social`, `clear`, `theme`, `whoami`, `date`, `echo`, `ls`, `pwd`, `cat`, `exit`, `sudo`.

## Features

- Tab completion for commands
- Up/Down arrow history
- Light and dark themes
- Click anywhere to focus the input
- ASCII banner shrinks on mobile
- No data leaves the browser

## Tech

- Single HTML file, ~400 lines
- Vanilla JS, no frameworks, no dependencies
- WCAG AA contrast on both themes
- Tested in current Chrome, Firefox, Safari

## What it doesn't do

- No real shell. Commands are mapped 1:1 to handlers; no `|`, `>`, `;` chaining.
- No file system. `cat about` works because there's an `about` command, not because there's a file.
- No autocomplete for command arguments.
- No persistent history across sessions (in-memory only).

## License

MIT. See [LICENSE](LICENSE).

## Related

- [single-file-saas-template](https://github.com/0xelitesystem/single-file-saas-template), ship a SaaS in one HTML file
- [oss-readme-template](https://github.com/0xelitesystem/oss-readme-template), battle-tested README structure
- [og-image-generator](https://github.com/0xelitesystem/og-image-generator), generate Open Graph cards
