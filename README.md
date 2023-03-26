# iOSProjectScripts

## 1. unused.rb

I took this script from: https://github.com/PaulTaykalo/swift-scripts and added a few things.

- Support for name arguments
- Add previews structs avoiding this false positive

### How to used it

```
ruby unused.rb
```

for larger projects you can especify the forlder

```
ruby unused.rb -d myFolder/anotherFolder
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
    ruby unused.rb -env xcode
else
    echo "unused.rb doesn't exist"
fi
```

Next steps:

- Adding git diff support
