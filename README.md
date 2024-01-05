# ManMan

ManMan (the manpage manual) is a simple shell script that provides a user-friendly interface for browsing and reading manual pages (man pages) using `fzf`, the command-line fuzzy finder.

## Current Features

- **Fuzzy searching**: ManMan uses `fzf` to provide a fuzzy-searchable list of man pages. You can type any part of the name or description of a man page, and `fzf` will show the matching man pages.
- **Previewing**: ManMan uses `fzf`'s preview feature to show a preview of the selected man page.
- **Section filtering**: ManMan supports the `-s` option to limit the search to a specific section of the man pages.

## Requirements

- `fzf`: ManMan uses `fzf` to provide a user-friendly interface for browsing man pages. You must have `fzf` installed to use ManMan.
- `man`: ManMan uses the `man` command to display man pages. You must have the `man` command available on your system to use ManMan.
- `apropos`: ManMan uses the `apropos` command to search for man pages. You must have the `apropos` command available on your system to use ManMan.

## Usage

To use ManMan, simply run the script with no arguments to browse all man pages:

```shell
./manman.sh
```

To limit the search to a specific section, use the `-s` option followed by the section number:

```shell
./manman.sh -s 1
```

Add an alias to your `.zshrc` or `.bashrc` file in a one-liner:

**zsh**
```shell
$ echo "alias manman=\"$(pwd)/manman.sh\"" >> ~/.zshrc
```

**bash**
```shell
$ echo "alias manman=\"$(pwd)/manman.sh\"" >> ~/.bashrc
```


## Future Improvements

- **Name searching**: In a future version, ManMan will be modified to use the `man -k` command instead of `apropos`. This will allow ManMan to search the names of man pages as well as their descriptions, making it easier to find specific man pages.
- **Improved error handling**: Future versions of ManMan will include improved error handling to provide more informative error messages when something goes wrong.
- **Customization**: Future versions of ManMan may include options to customize the appearance and behavior of `fzf`, such as changing the height of the `fzf` window or the prompt text.

## Installation

To install ManMan, simply download the `manman.sh` script and make it executable:

```shell
chmod +x manman.sh
```

You can then run ManMan by executing the `manman.sh` script.
