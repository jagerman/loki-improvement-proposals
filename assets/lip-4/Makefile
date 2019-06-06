# Simple makefile to build a nice HTML from the multimarkdown source and hack together a decent
# github-flavoured markdown

all: blink.html ../../LIPS/LIP-4.md

blink.html: Blink.md title.html pandoc.css footnotes.css blink.svg quorums.svg blink-quorum-conns.svg quorum-critical.svg
	pandoc -f markdown -t html5 -M pagetitle="Loki Blink Design" --self-contained --toc --css=pandoc.css --css=footnotes.css -B title.html -o $@ $<

%.svg: %.dot
	dot -Tsvg -o$@ $<

../../LIPS/LIP-4.md: Blink.md github-preamble.md blink.svg quorums.svg blink-quorum-conns.svg quorum-critical.svg
	pandoc -f markdown -t gfm -B github-preamble.md -o lip4.md.tmp $<
	perl -pi -e 's/\\\[(\d+)\\\]/[\\[$$1\\]](#user-content-fn$$1)/g; BEGIN{$$FN=0} if (not $$FN and /^1\.\s+This split/) { $$FN=1; print "# *Footnotes*\n\n<ol>\n"; } s/^(\d+)\./<li id="fn$$1">/ if $$FN' lip4.md.tmp
	perl -pi -e 's!\]\((\S+\.svg)\)!](../assets/lip-4/$$1)!' lip4.md.tmp
	perl -e '$$C=""; %M=(); while(<>) { $$C .= $$_; if (/^#+\s+(\d+(?:\.\d+)*)\s+(.*)/) { $$f = ($$2 =~ tr/A-Za-z -//cdr =~ tr/A-Z -/a-z\--/dsr); $$t = ($$1 =~ tr/0-9//cdr) . "-" . $$f; $$M{$$f} = $$t; } } my $$r = join "|", map quotemeta, keys %M; $$C =~ s/\]\(#($$r)\)/](#$$M{$$1})/g; open my $$h, ">", "$@"; print $$h $$C' lip4.md.tmp
	rm -f lip4.md.tmp

clean:
	rm -f ../../LIP-4.md *.svg blink.html
