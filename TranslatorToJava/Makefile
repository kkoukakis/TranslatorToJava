#Vars
SCANNER = Scanner.java
PARSER = Parser.java
SYM = Sym.java
OUTPUT = Output.java
MESSAGE = You can type make compile, run, clean


#Commands
all: compile

compile:
	jflex scanner.flex
	java -jar ../java-cup-11b.jar -interface -parser Parser parser.cup
	javac -cp ../java-cup-11b-runtime.jar *.java
	@echo build done.

help:
	@echo $(MESSAGE)

run:
	java -cp ../java-cup-11b-runtime.jar:. Main > Output.java

clean:
	rm -f *.class *~
	rm -f $(SCANNER)
	rm -f $(PARSER)
	rm -f $(SYM)
	rm -f $(OUTPUT)
	@echo clean done.
