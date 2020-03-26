# TranslatorToJava

 Implementation of a parser and translator for a language supporting string operations. The language supports concatenation (+) and "reverse" operators over strings, function definitions and calls, conditionals (if-else i.e, every "if" must be followed by an "else"), and the following logical expression:

    `is-prefix-of (string1 prefix string2): Whether string1 is a prefix of string2.`

 All values in the language are strings.

 The precedence of the operator expressions is defined as: precedence(if) < precedence(concat) < precedence(reverse).

 Your parser, based on a context-free grammar, will translate the input language into Java. You will use JavaCUP for the generation of the parser combined either with a hand-written lexer or a generated-one (e.g., using JFlex, which is encouraged).

 You will infer the desired syntax of the input and output languages from the examples below. The output language is a subset of  Java so it can be compiled using javac and executed using Java or online Java compilers like this, if you want to test your output.

 There is no need to perform type checking for the argument types or a check for the number of function arguments. You can assume that the program input will always be semantically correct.

 A s with the first part of this assignment, you should accept input programs from stdin and print output Java programs to stdout. For your own convenience you can name the public class "Main", expecting the files that will be created by redirecting stdout output to be named "Main.java".. In order to compile a file named Main.java you need to execute the command: javac Main.java. In order to execute the produced Main.class file you need to execute: java Main.

 To execute the program successfully, the "Main" class of your Java program must have a method with the following signature: public static void main(String[] args), which will be the main method of your program, containing all the translated statements of the input program. Moreover, for each function declaration of the input program, the translated Java program must contain an equivalent static method of the same name. Finally, keep in mind that in the input language the function declarations must precede all statements.
