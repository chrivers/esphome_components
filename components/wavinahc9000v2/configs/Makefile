CHANNELS         := $(shell seq -f "channel_%02g.yaml"         1 16)
CHANNELS_COMFORT := $(shell seq -f "channel_%02g_comfort.yaml" 1 16)

all: $(CHANNELS) $(CHANNELS_COMFORT)

channel_%.yaml: channel_xx.yaml.tmpl
	sed -re 's/(channel[_ ])01/\1$*/' $< > $@

channel_%_comfort.yaml: channel_xx_comfort.yaml.tmpl
	sed -re 's/(channel[_ ])01/\1$*/' $< > $@
