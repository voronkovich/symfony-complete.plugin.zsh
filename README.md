# Universal ZSH completion for Symfony applications

A zsh plugin for the [symfony/console](https://symfony.com/doc/current/components/console.html) based applications (e.g. `composer`, `bin/console`, `artisan`, `php-cs-fixer` and etc.). This plugin supports autocompletion for subcommands (`composer req`) and GNU-style options (`--help`).

## Installation

[Antigen](https://github.com/zsh-users/antigen):

```sh
antigen bundle voronkovich/symfony-complete.plugin.zsh
```

Or clone this repo and add this into your `.zshrc`:

```sh
source path/to/cloned/repo/symfony-complete.plugin.zsh
```

## Usage

Enable autocompletion in your `.zshrc` for all needed commands:

```sh
autoload _symfony_complete

# Yes, it can complete symfony binary too :)
compdef _symfony_complete symfony
compdef _symfony_complete composer
compdef _symfony_complete console
compdef _symfony_complete artisan
compdef _symfony_complete phpstan
compdef _symfony_complete php-cs-fixer
compdef _symfony_complete phpspec
```

## License

Copyright (c) Voronkovich Oleg. Distributed under the MIT.
