# whereami

When switching between projects you often want to change who is going to be attributed to your commits.

For example, one moment you are working on a work project, and the next moment you are fixing a bug in your personal project.

The key piece of information that needs to be switched out in this situation is your Git config settings.

So, before you commit:

```
whereami home
```

or if at work:

```
whereami work
```

## Installation
This is a Perl script. Tested on 5v20.

Put this on your `PATH` so it can be invoked in the same spirit as `whoami`.

The checked-in version already has the executable bit set.

## Configuration
Edit config file: `~/.whereami.properties`

Space-delimited format:
```
work
  name Jonathan Brink
  email Jonathan.Brink@mycompany.com

home
  name Johnny Brink
  email jonathandavidbrink@gmail.com
```


