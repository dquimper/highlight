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
cat README.md | highlight -r word1 # Will make word1 red
cat README.md | highlight -b word2 # Will make word2 blue
cat README.md | highlight -i word2 # Will inverse the colors of word2
cat README.md | highlight -g word3 -y word4 # Will make word3 green and word4 yellow
cat README.md | highlight -r word1 -r word2 # Will make word1 and word2 red
```

It's also possible to use regular expressions for the matches.

```
cat README.md | highlight -r "word1|word2" # Will make word1 and word2 red 
cat README.md | highlight -g "word[12]" # Will make word1 and word2 green 
```
