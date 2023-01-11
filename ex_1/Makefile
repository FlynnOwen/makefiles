# Variables are set using := -- these are strings and can be referenced by using $(files)
files := file1 file2

# First command is default - i.e. this is run if just 'make' is executed
testfile: # anything before : is a 'target' - this is a file name (separated by spaces)
	touch testfile
# Anything below the targets and indented, are 'commands'. These are in shell.
# Typically, when commands are run, they create a file, which may be a 'target' itself.

write_hello: testfile # Second argument (after :) is a pre-requisite. These need to exist before this target can run.
# This command make command will only run if if write_hello doesn't exist, or testfile.txt is newer than write_hello
	echo 'hello'

clean:
	rm testfile blah blah.c blah.o

# Below is a full example:
blah: blah.o
	cc blah.o -o blah # Runs third

blah.o: blah.c
	cc -c blah.c -o blah.o # Runs second

# Typically blah.c would already exist, but I want to limit any additional required files
blah.c:
	echo "int main() { return 0; }" > blah.c # Runs first