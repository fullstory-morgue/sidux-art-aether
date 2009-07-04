#!/usr/bin/make -f

ICONS= icon
THEME= sidux-aether
CONTROLDIR= 1024x768
ANIMCREATOR= ./svg-anim.pl

all: $(ICONS)

icon:
	$(RM) -r $(THEME)/$(CONTROLDIR)
	mkdir -p $(THEME)/$(CONTROLDIR)
	$(ANIMCREATOR) frames=30 effect=opacity:cycle < $@.svg > $@_anim.svg
	inkscape --without-gui --export-png="$(THEME)/$(CONTROLDIR)/$@_anim.png" $@_anim.svg

clean:
	$(RM) -r $(THEME)
