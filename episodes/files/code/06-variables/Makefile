include config.mk

# Generate summary table.
results.txt : $(ZIPF_SRC) isles.dat abyss.dat last.dat
	$(LANGUAGE) $^ > $@

# Count words.
.PHONY : dats
dats : isles.dat abyss.dat last.dat

%.dat : $(COUNT_SRC) books/%.txt
	$(LANGUAGE) $^

.PHONY : clean
clean :
	rm -f *.dat
	rm -f results.txt
