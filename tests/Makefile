include ../Makedefs

ERL_FILES := $(wildcard *.erl)
BEAM_TARGETS := $(addsuffix .beam, $(basename $(ERL_FILES)))

default: all

all: $(BEAM_TARGETS) ;

%.beam: %.erl
	erlc -W $<

clean: 
	rm -f $(BEAM_TARGETS)
	rm -f ./*.*~

clobber: clean ;

install: all
	install -m 0755 $(ERL_FILES) $(SRC_DIR)
	install -m 0755 $(BEAM_TARGETS) $(EBIN_DIR)

uninstall: ;
