# iOSProjectScripts

## 1. unused.rb

I took this script from: https://github.com/PaulTaykalo/swift-scripts and added a few things.

- Support for name arguments
- Added previews structs avoiding this false positive
- added git diff from a specific branch

### How to used it

```
ruby unused.rb -d /project-folder
# For bigger projects when you need to valid a specific folder
ruby unused.rb -d /project-folder/specific-folder
```

Validate only files you have modified, `--git-diff-develop` this flag will take the files changed between current branch and `-rbranch` flag

if `-rbranch` is not specified it will be `main`

```
ruby unused.rb --git-diff-develop -d /my-project-folder/ -b develop
```

looking for help?

```
ruby unused.rb -h
```

using on xcode file="unused.rb" will depends on the path of the file

```
file="unused.rb"
if [ -f "$file" ]
then
    echo "$file found."
    ruby unused.rb -e xcode -d .
else
    echo "unused.rb doesn't exist"
fi
```

Next steps:

- Add more validations
- Add a better xcode support

## Dependencies

```
bundle install
```

https://github.com/ruby/optparse

https://github.com/ruby-git/ruby-git
