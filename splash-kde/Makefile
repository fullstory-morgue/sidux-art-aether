#!/usr/bin/make -f

NAME= background
THEME= sidux-aether
SIZES= 400x250 800x480 800x600 1024x768 1280x800 1280x1024 1440x900 1600x1200 1920x1200 
SVG= $(NAME).svg

all: $(SIZES)

400x250:
	mkdir -p $(THEME)/$@
	$(RM) $(THEME)/$@/$(NAME).png
	inkscape --without-gui --export-width=$(firstword $(subst x, ,$@ )) \
		--export-height=$(lastword $(subst x, ,$@ )) \
		--export-png="$(THEME)/Preview.png" $(SVG)

1280x1024:
	mkdir -p $(THEME)/$@
	$(RM) $(THEME)/$@/$(NAME).png
	inkscape --without-gui --export-width=$(firstword $(subst x, ,$@ )) \
		--export-height=$(lastword $(subst x, ,$@ )) \
		--export-area=210:0:1710:1200 \
		--export-png="$(THEME)/$@/$(NAME).png" $(SVG)

800x600 1024x768 1600x1200:
	mkdir -p $(THEME)/$@
	$(RM) $(THEME)/$@/$(NAME).png
	inkscape --without-gui --export-width=$(firstword $(subst x, ,$@ )) \
		--export-height=$(lastword $(subst x, ,$@ )) \
		--export-area=160:0:1760:1200 \
		--export-png="$(THEME)/$@/$(NAME).png" $(SVG)

800x480 1280x800 1440x900 1920x1200:
	mkdir -p $(THEME)/$@
	$(RM) $(THEME)/$@/$(NAME).png
	inkscape --without-gui --export-width=$(firstword $(subst x, ,$@ )) \
		--export-height=$(lastword $(subst x, ,$@ )) \
		--export-png="$(THEME)/$@/$(NAME).png" $(SVG)

clean:
	$(RM) -r $(THEME)
