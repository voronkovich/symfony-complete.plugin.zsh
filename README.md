# Universal ZSH completion for Symfony applications

[![Tests](https://github.com/voronkovich/symfony-complete.plugin.zsh/actions/workflows/tests.yaml/badge.svg)](https://github.com/voronkovich/symfony-complete.plugin.zsh/actions/workflows/tests.yaml)

A zsh plugin for the [symfony/console](https://symfony.com/doc/current/components/console.html) based applications (e.g. `composer`, `bin/console`, `artisan`, `php-cs-fixer` and etc.). This plugin supports autocompletion for subcommands (`composer req`) and GNU-style options (`--help`).

![Commands autocompletion](/screenshots/commands.png?raw=true "Commands autocompletion")
![Options autocompletion](/screenshots/options.png?raw=true "Options autocompletion")

## Installation

### [Antigen](https://github.com/zsh-users/antigen)

```sh
antigen bundle voronkovich/symfony-complete.plugin.zsh
```
### [Zplug](https://github.com/zplug/zplug)

```sh
zplug "voronkovich/symfony-complete.plugin.zsh"
```

### [Oh My Zsh](https://github.com/ohmyzsh/ohmyzsh)

```sh
git clone https://github.com/voronkovich/symfony-complete.plugin.zsh ~/.oh-my-zsh/custom/plugins/symfony-complete
```

Edit `.zshrc` to enable the plugin:

```sh
plugins=(... symfony-complete)
```

### Manual

Clone this repo and add this into your `.zshrc`:

```sh
source path/to/cloned/repo/symfony-complete.plugin.zsh
```

## Usage

Enable autocompletion in your `.zshrc` for all needed commands:

```sh
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
