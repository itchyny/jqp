# jqp 

a TUI playground for exploring jq. 

This application utilizes [itchny's](https://github.com/itchyny) implementation of `jq` written in Go, [`gojq`](https://github.com/itchyny/gojq).

## Installation

## Usage

```
➜ jqp --help
jqp is a TUI to explore the jq command line utility

Usage:
  jqp [flags]

Flags:
  -f, --file string   path to the input JSON file
  -h, --help          help for jqp
  -v, --version       version for jqp
```

`jqp` also support input from STDIN. 

```
➜ curl "https://api.github.com/repos/stedolan/jq/issues?per_page=2" | jqp 
```

## Keybindings 

| **Keybinding** | **Action** |
|:---------------|:-----------|
| `tab` | switch active section |
| `ctrl-s` | save output to file |
| `ctrl-c` | quit program |

### Query Mode

| **Keybinding** | **Action** |
|:---------------|:-----------|
| `enter` | execute query |
| `ctrl-a` | go to beginning of line |
| `ctrl-e` | go to end of line |
| `←`/`ctrl-b` | move cursor one character to left |
| `→`/`ctrl-f`| move cursor one character to right |
| `ctrl-k` | delete text after cursor line |
| `ctrl-u` | delete text before cursor |
| `ctrl-w` | delete word to left |
| `ctrl-d` | delete character under cursor |

### Input Preview and Output Mode

| **Keybinding** | **Action** |
|:---------------|:-----------|
| `↑/k` | up |
| `↓/j` | down |
| `ctrl-u` | page up |
| `ctrl-d` | page down |

## Built with:

- [Bubbletea](https://github.com/charmbracelet/bubbletea)
- [Bubbles](https://github.com/charmbracelet/bubbles)
- [Lipgloss](https://github.com/charmbracelet/lipgloss)
- [gojq](https://github.com/itchyny/gojq)


## Credits

- [jqq](https://github.com/jcsalterego/jqq) for inspiration
