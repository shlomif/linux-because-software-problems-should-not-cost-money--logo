SVG = linux-because-software-problems-should-not-cost-money--logo.svg
PNG = $(SVG).png
JPEG = $(SVG).jpg
WEBP = $(SVG).webp

WIDTH = 1200

all: $(PNG) $(JPEG) $(WEBP)

$(PNG): $(SVG)
	inkscape --export-filename=$@ --export-type=png --export-width=$(WIDTH) --export-background='#e7f700' --export-background-opacity=1.0 $<

$(JPEG): $(PNG)
	gm convert $< $@

$(WEBP): $(PNG)
	gm convert $< $@

clean:
	rm -f $(PNG) $(JPEG) $(WEBP)

# sky is: https://www.shlomifish.org/open-source/projects/sky/
upload: all
	sky up $(SVG)
	sky up -x $(WEBP)

# vim:ft=make
#
