# persona

When switching between projects you often want to change who is going to be attributed to your commits.

For example, one moment you are working on a work project, and the next moment you are fixing a bug in your personal project.

The key piece of information that needs to be switched out in this situation is your Git config settings as well as your active SSH keys.

So, before you commit:

```
persona home
```

or if at work:

```
persona work
```

## Installation
This is a Perl script that can be placed on your `PATH`. Tested on 5v20.

The checked-in version already has the executable bit set.

## Configuration
Edit config file: `~/.persona.properties`

Space-delimited format:
```
work
  name Jonathan Brink
  email Jonathan.Brink@mycompany.com

home
  name Johnny Brink
  email jonathandavidbrink@gmail.com
```

### File Swapping

Place ssh keys, and .npmrc files in directories matching their "place", in `~/.esesh`.

For example:
```sh
$ tree ~/.esesh
/home/user/.esesh
├── home
│   ├── id_rsa
│   └── id_rsa.pub
└── work
    ├── id_rsa
    └── id_rsa.pub
```

## Features

### update
Update commit author and comitter in a "rebase" fashion.

```
persona --update HEAD~~~
```

Automates:
```
git rebase --interactive $ref --exec "git commit --amend --reset-author -CHEAD"
```

## License
[BSD-2-Clause](http://spdx.org/licenses/BSD-2-Clause)
