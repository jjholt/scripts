# scripts

Collection of scripts to make navigating bibliographies a lot easier.

## Requirements

[`fzf`](https://github.com/junegunn/fzf/)

[`rga`](https://github.com/phiresky/ripgrep-all)

## Zathura-go-to

`zathura-go-to` is a tool to control page changes in Zathura from the terminal.
The motivation for it is to enable creating a link inside a latex file that moves you to the correct page.
It uses `dbus` via `busctl` to request zathura to change a page. 

### Usage
To change the page on an open instance of zathura, use:
```bash
$zathura-go-to 5
```
If there are multiple instances open, it will enumerate them for you to choose which one should receive the command:
```bash
Please choose the document index:
[1]: /path/to/file1.pdf
[2]: /path/to/file2.pdf
```

## Bibsearch
`Bibsearch` is a first attempt at fuzzy finding through a list of pdfs. If there is a match, then it opens the pdf and highlights your query; if it doesn't find any file, then it searches for your query on the internet.
