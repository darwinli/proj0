Enigma Project
=====

Enigma Project - Progressive Substitution Cryptography

 java enigma.Main
 
Runs the program.

Initialize the machine by giving a setting to the rotors. The setting command must have the syntax

B GAMMA I II III
with proper spacing and case. Rotor 'B' may be replaced with name 'B' or 'C' and 'BETA' may be replaced with 'BETA' or 'GAMMA'. Any of the next three rotors may be replaced with I - VIII. Encryption pathways can be found in the file PermutationData.java; however, the point of this project is to encrypt and decrypt.

After setting the machine, typing any letters or strings of letters will yield the encrypted output. By resetting the machine to the original settings, one can decrypt the output by feeding it back into the Enigma machine. An example: Input:

B BETA I II III AAAA Hello world
Output:

ILBDA AMTAZ

Input:

B BETA I II III AAAA ILBDA AMTAZ
Output:

HELLO WORLD

See http://en.wikipedia.org/wiki/Enigma_machine for more background information

enigma Directory containing the enigma package:

enigma/Main.java Contains the main procedure: enigma.Main.main. enigma/Machine.java Objects that model the Enigma machines. enigma/Rotor.java The objects that model the rotors that are part of the Enigma machines. enigma/Reflector.java A special type of Rotor that lies at the end. enigma/PermutationData.java Static data describing the Enigma rotors and reflectors.

tests Directory for test files. Contains files *.inp, *.out, and *.err, intended as test input files, expected output files, and erroneous input files for the enigma program. The Makefile is set up so that 'gmake check' runs each .inp file through your program and compares the results to the corresponding .out file. It also runs each .err file through your program and checks that the program reports an error according to the project specification.

tests/trivial.in, tests/trivial.out Sample test file input and output.
