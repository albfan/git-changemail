PANDOC ?= /usr/bin/pandoc
MANSECTION ?= 1
PANDOCFLAGS=--metadata title=GIT-CHANGEMAIL \
	    --metadata date=20/09/2021 \
	    --metadata hyphenate=false \
	    --metadata=adjusting=l \
	    --metadata footer="Git Changemail 1.0" \
	    --metadata header="Git Changemail" \
	    --metadata section=$(MANSECTION)


PANDOC_COMMAND = $(PANDOC) --standalone $(PANDOCFLAGS) --to man

%.$(MANSECTION): %.$(MANSECTION).md
	$(PANDOC_COMMAND) $< -o $@

dist_man1_MANS = git-changemail.1
