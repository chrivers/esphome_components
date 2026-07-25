CHANNELS_COMFORT := $(shell seq -f "channel_%02g_comfort.yaml" 1 16)

all: $(CHANNELS_COMFORT)

channel_%_comfort.yaml: channel_xx_comfort.yaml.tmpl
	sed -re 's/(channel[_ ])01/\1$*/' $< > $@
