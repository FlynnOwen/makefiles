# Using 'all' is a way to specify that all pre-requisite make commands should be run
all: one two three

one:
	touch one
two:
	touch two
three:
	touch three

# wildcards (denoted 'wildcard */%') are a way to string match in makefiles.
# Print out file information in any folder prefixed with ex_
print: $(wildcard ex_*)
	ls -la  $?

clean:
	rm -f one two three