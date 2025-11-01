# Makefile for lab_5_malloclab submission

TURNIN_DIR := ../generated-turnins/lab5_malloclab
BASENAME   := lab_5_malloclab

# Determine next available zip index
NEXT_INDEX := $(shell \
	mkdir -p $(TURNIN_DIR); \
	i=1; \
	while [ -e "$(TURNIN_DIR)/$(BASENAME)_$$i.zip" ]; do \
		i=$$((i+1)); \
	done; \
	echo $$i )

ZIPFILE := $(TURNIN_DIR)/$(BASENAME)_$(NEXT_INDEX).zip

.PHONY: submit

submit:
	@echo "Creating submission archive: $(ZIPFILE)"
	@mkdir -p $(TURNIN_DIR)
	@zip -r "$(ZIPFILE)" src > /dev/null
	@echo "Submission archive generated: $(ZIPFILE)"
