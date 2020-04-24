# Split Semantic Version

If you have a make variable that is set to a semantic verison, you
can split the parts using make text functions.

```make
VERSION := 1.2.3
VERSION_PARTS := $(subst ., ,$(VERSION))  # 1 2 3

MAJOR := $(word 1,$(VERSION_PARTS))  # 1
MINOR := $(word 2,$(VERSION_PARTS))  # 2
MICRO := $(word 3,$(VERSION_PARTS))  # 3
```

## References
- https://gist.github.com/grihabor/4a750b9d82c9aa55d5276bd5503829be
- https://www.gnu.org/software/make/manual/html_node/Text-Functions.html
