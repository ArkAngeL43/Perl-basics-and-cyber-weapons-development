# Perl-basics-and-cyber-weapons-development

```

                                                                                                          
             _     ___     ___   ___ ___ ___                _                                             
 ___ ___ ___| |___|  _|___|_  | | . | . |_  |   ___ ___ _ _| |_ ___ ___ ___ _ _ _ ___ ___ ___ ___ ___ ___ 
| . | -_|  _| |___|_  |___|_| |_|_  | . | | |  |___|  _| | | . | -_|  _|___| | | | -_| .'| . | . |   |_ -|
|  _|___|_| |_|   |___|   |_____|___|___| |_|      |___|_  |___|___|_|     |_____|___|__,|  _|___|_|_|___|
|_|                                                    |___|                             |_|              
```

# Introduction to this repo 

The first thing i would like to state, is the choice to use a certian language for everyday use is bias, which means some things as described for perl will be based off of my personal experience and my personal opinion of the language, ofc when we do leave the introduction to this repo and perl itself I will try my best to be as professional as i can when explaining to you how perl works in the best of ways and exactly how this can work in ways.

> What is perl, and why was/is it used 

Perl is a programming language which is interpretted meaning there is no binary to it unless you install a third party library to do so, kinda like the way python is. This language also runs off of a mix of syntaxes when it comes to languages like Fortran, PHP, SED, BASIC, and powershell. Perl in my opionion is a very very weird language, however if you come from a long line of programmers or have haed experience in languages like Python, R, PHP, JS, Java, Fortran ETC then it becomes quite easy to understand as well as write in. The cool thing about perl is it has some intriguing decleration points like using MY to declare a private variable or naming a function like `sub`

Perl was originally used in the early 2000's as a web development language like PHP is, not on the frontend but on the backend as perl has some amazing functions and base alternatives for making programs that can easily and successfully connect to the client very fast. Another prime use for perl ( even the modern day perl RAKU ) is CGI scripting and Practical Extraction and Reporting, this means that perl is a language used in backend systems to execute other programs. Because perl is so good with CGI scripting and server side development, this also means it is very practicle to use it for cyber weapons, I myself personally find it as a great language to use for exploitation. 

> What is perl used best for in hacking 

Perl designed for mainly web applications would specialize best in web exploitation, things like SQL injection, RFI/LFI, Vulnerability scanning and recon, as well as a few other side things. While perl is not the most modern and liked language in 2022 or in this case the modern era it is still used in legacy systems such as school systems, government agencies, and more. 

> Perls extension types 

- .CGI Defined the common gateway interfearence scripting file, this is what most legacy web servers will use to execute subroutines or other programs 

- .PL this is the standard perl file, you would run this file as perl filename.pl

- .PM this is the standard Perl Module file, what you will use to write and define your own modules in and for perl these normally are not executed as perl file.pm they are rather imported into other perl files and ran that way, however if you wanted to run an example perl module you could use
 
- .t which is the testing module file which perl will use to run module tests which are usually used to test if modules work on other peoples machines and if not it will throw the report out and attempt to install the module or thing that was missing from that file if it was structured that way 


# Starting out with perl, warnings, usages, and how this language could help 

While this language is not in use anymore it can definitely help you understand and explore different syntaxes and how other languages work. In this sengment i will be giving you some warnings before diving into the language such as help and other things which can make this language easy to learn, as well as some things and concepts i missed with perl.  

> Where to get help with perl5

So in todays time like fortran not many people program in perl anymore, in fact its kinda getting phased out if you are not a legacy developer for other people or other companies, this means that help is very rare ( and i wish i knew that before going into the language ), there will be alot of books still out there however some are rare and others are just not the best of knowlege given they most likely apply to perl3 or the first version of perl. When i first started this language i did not know properly where to go for help, given i knew only a few people who were good at perl and even then i could not talk to them all the time. This pushed me away from the language and made me hate it, the more i hated it the more i got used to it given my entire weaponry and SQL database i had setup was managed by this language. Some tips to know about this language before taking a full dive into it is that it is a weird and hard language to get into if you have not had any previous experience with languages like PHP, its syntax personally i do not like and many will gladly agree with me, however you eventually find the language useful in many other cases so you choose to deal with it.

Some sources for the perl programming language are as follows 

- Fixing errors: Stackoverflow
- Documentation: https://perldoc.perl.org/
- CPAN         : https://www.cpan.org/doc/index.html
- Module files : https://perldoc.perl.org/perlmodstyle
- Libraries    : https://metacpan.org/pod/module::name
( replace module::name with something like Net::Server or the library name )


# the basics of the perl programming language 

Get ready to experience programming on drugs XDDD

> Running perl files

```pl
perl filename.pl
```
> Installing third party perl modules

```pl
sudo cpan install module::name
```

example

```pl
sudo cpan install Getopt::Std;
```

sudo is not needed but it will ask you what you want like for it to be installed via root, or no root, or other type premissions

> Writing some begginer level programs to understand how perl works

Perl is a wacky language, however lets start by making some example programs, i personally feel the best way to experience how a language works is by working with the basics, not just hello world but http servers, making url requests, using third party libraries, writing and outputting files etc so in this section we will be writing 5+ scripts to get you familiar with perl 

before we start writing im going to be giving you a small sheet of some simple perl functions or statements in a table 

| Function |                                  Description                                 |              Usage / Syntax                    |
| -------- | ---------------------------------------------------------------------------- | ---------------------------------------------- |
| print""; | Will output a statement to the standard I/O ( Input Output )                 | print "something";                             |
| my       | My declares a public variable                                                | my $varname = "something"                      |
| sub      | Sub declares the start of a subroutine                                       | sub subroutinename()                           |
| use      | Standard import function for libraries                                       | use module::name                               |
| $_       | The default input and pattern-searching space                                | print $_;                                      |
| or       | The defualt or statement in perl                                             | or die $!;                                     |
| die      | kill the current function/script and write a message to a user               | die "some error message to write to the IO"    |
| $!       | Standard error message or what went wrong                                    | or die (Error -> $!)                           |
| say      | Say is a feature which eliminates the use for the \n at th end of print"";   | say "name random things";                      |
| @        | initates an array                                                            | @name($value,);                                |

> Additional operators in perl 

| push()

the `push()` operator  is used to append an element to the end of an array, kinda the same as .append() in other languages 
its syntax is as follows 

```pl
my @array_name
push(@array_name, 'variable, element, etc');
push(@array_name, ('you', 'can', 'also', 'append', 'multiple', 'values', 'like', 'this'))
```

if you want to push multiple values you must have a () encapsulating the variables, if you are just appending only one variable then () is not needed an example of non encapsulation is at the top, and encapsulation at the bottom, notice the difference?

> Boolean logic

<h5> Mathematical </h5>

|    Operator   | Description of its usage and what it does                                                                           |
| ------------- | ------------------------------------------------------------------------------------------------------------------- |
|      =        | Assigns a variable to a value                                                                                       |
|     ==        | test if a variable is equal to a value, can not be used in checking string statements ex if ($varname == $varname2) |
|      !        | defines NOT, something like != can be used in a statement like if (!$var) {print "hello world";}                    |
|     eq        | checks if a string is equal to another variable, is used usually as a replacement for eq                            |
|      >        | Is greater than                                                                                                     |
|      <        | defines a variable as less than                                                                                     |
|      gt       | checks if a string or variable is greater than another, ex: $c = $a gt $b                                           |
|      it       | checks if a string or variable is LESS than another same syntax as GT                                               |
|      >=       | Greater than or equal to                                                                                            |
|      <=       | Less than or equal to                                                                                               |
|      gte      | greater than or equal to                                                                                            |
|      lte      | less than or equal to, kinda like eq is to == but instead with >= is gte and <= lte                                 |
|      ~        | Often used with regular expressions, is often used as the perl binding operator to bind or compile regex ( sense )  | 
|      !~       | Does not equal with regex                                                                                           |
|      =~       | equal with regex                                                                                                    |

- we will use these later on keep this table in mind 

<h5>Statements</h5>

|    Operator   | Description of its usage and what it does                                                                           |
| ------------- | ------------------------------------------------------------------------------------------------------------------- |
|      if       | Checks if a value is eq, not eq, false, true, etc etc or equal to something syntax if (condition == second) {code}  |
|    unless     | represents elif or something like elif unless ($variable >= 900) {do something}                                     |
|     AND OR    | can be represented as &&, and, ||, or is used like if (var < 1 && var2 < 1) {code}                                  |
|    golfing    | Not an operator but a term,  applies to condensing a boolean statement into one line print"\n" unless ($age >= 18); |                           |     for       | represents a continuous loop, for something = 0; something < something                                              |
|   foreach     | defines a for loop which is usually used to itterate over lists or large outputs                                    |
|   STDIN       | Standard input syntax <> example: print"enter something"; my $something = <>;                                       |
 

there are much more but i will go into that later, now lets start to write our script 

so to first start off we will be using perls for loops to infinitely count inside of a for loop, this will be called under a subroutine to also get you familiar with how the functions work

```pl
#! /usr/bin/perl

# useage of the perl shabang
use strict;
# using strict, a library to help you write secure code, basically stops you from using 
# functions or operators that can behave weirdly inside of a perl script

my @s = qw/ something, something2, something3, something4, something5, d, d, r, rg, gd, g, ghg, g, rg, rg, drg, drg / ;
my $count = 0 ;
#The qw operator is used to extract each element of the given string as it is in an array of elements in single-quote
# the @s defines an array
# using MY to declare a public variable which is visible to all classes 

# use the sub function to define main as a subroutine
sub main {
    {
        # define the for loop, foreach is foreach in range of $e in the array @s
        foreach my $e(@s)
        {
            # for every , will count as 1, if they are not seperated it will not count
            print "Number -> ", $count++, " Holds letter -> $e\n"  ;
                                # count++ for every strig   #$e defines the character, or string inside of the array
        }
    }
}

main();
# call the main function
```

this should be easy to understand given the notes, the summary would be we decalre a array by using the `@`, then use the `QW` operator which will split every string, char, int, etc etc in that array seperated like `something, something2` etc, then declares a foreach, for every `$e ( every word ) in the array (@s)` it will use the `++ variable` to count `count++` to add how much letters there are in the array or phrases, then outputs it. `$e` will be the letter it is at, which produces the folloing output 

```pl
Number -> 0 Holds letter -> something,
Number -> 1 Holds letter -> something2,
Number -> 2 Holds letter -> something3,
Number -> 3 Holds letter -> something4,
Number -> 4 Holds letter -> something5,
Number -> 5 Holds letter -> d,
Number -> 6 Holds letter -> d,
Number -> 7 Holds letter -> r,
Number -> 8 Holds letter -> rg,
Number -> 9 Holds letter -> gd,
Number -> 10 Holds letter -> g,
Number -> 11 Holds letter -> ghg,
Number -> 12 Holds letter -> g,
Number -> 13 Holds letter -> rg,
Number -> 14 Holds letter -> rg,
Number -> 15 Holds letter -> drg,
Number -> 16 Holds letter -> drg
```
