UTILSDIR	:= ../../utils

PERL5LIB	:= $(UTILSDIR)/sin
export PERL5LIB

MAINTAINED	:= $(patsubst %.in,%,$(wildcard *.in))

all: $(MAINTAINED)

$(MAINTAINED): %: %.in
	@$(UTILSDIR)/sin/sin -I $(UTILSDIR)/gist/gist.d $< >$@ || { rm -f $@; exit 1; }
