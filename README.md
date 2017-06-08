# highlight
Simple command line tool to **highlight** text from stdin.

## Help

```
$ ./highlight -h
Highlights word from STDIN using ANSI color codes.
Usage: highlight [options]
Options:
    -r, --red [WORD]                 Makes WORD red
    -g, --green [WORD]               Makes WORD green
    -b, --blue [WORD]                Makes WORD blue
    -y, --yellow [WORD]              Makes WORD yellow
    -i, --inverse [WORD]             Inverses foreground & background colors of WORD
    -h, --help                       Prints this help
```

### Examples

```
cat somefile | highlight -r word1 # Will make word1 red
cat somefile | highlight -b word2 # Will make word2 blue
cat somefile | highlight -g word3 -y word4 # Will make word3 green an word4 yellow
cat somefile | highlight -r word1 -r word2 # will make word1 and word2 red
```
