IniParser
=========

This is a ery simple parser for ini files.

In order to write an ini file:

IniParser parser = new IniParser();
parser.addSection("Section1");
parser.addString("Section1", "test", "Hello");
parser.writeFile(ini);

In order to parse an ini file:

IniParser parser = new IniParser();
parser.parseFile(path_to_ini_file);
string s1 = parser.getString("Section1", "test");

The parser support comments in ini files but only rewrite them (on the output file) if the comment is in a new line (comments in the same line that ini options wouldn't rewrite)
