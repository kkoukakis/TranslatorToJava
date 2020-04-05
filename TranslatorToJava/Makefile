#Vars
SCANNER = Scanner.java
PARSER = Parser.java
SYM = Sym.java

OUTPUT = Output
OUTPUTJAVA = Output.java
OUTPUTCLASS = Output.class

MESSAGE = You can type make compile, run, clean


#Commands
all: compile

compile:
	jflex scanner.flex
	java -jar ../java-cup-11b.jar -interface -parser Parser parser.cup
	javac -cp ../java-cup-11b-runtime.jar *.java  
	@echo build done.
	
compile-Xlint:
	jflex scanner.flex
	java -jar ../java-cup-11b.jar -interface -parser Parser parser.cup
	javac -cp ../java-cup-11b-runtime.jar *.java -Xlint:deprecation
	@echo build done.


help:
	@echo $(MESSAGE)

run:
	java -cp ../java-cup-11b-runtime.jar:. Main > Output.java

#COMMANDS FOR OUTPUT
out:
	javac Output.java
	@echo output build done.


out-run:
	java $(OUTPUT)

out-clean:
	rm -f $(OUTPUTJAVA)
	rm -f $(OUTPUTCLASS)
	@echo out clean done.

clean:
	rm -f *.class *~
	rm -f $(SCANNER)
	rm -f $(PARSER)
	rm -f $(SYM)
	rm -f $(OUTPUTJAVA)
	@echo clean done.
