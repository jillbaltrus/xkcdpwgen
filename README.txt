The xkcdpwgen program generates a strong, random password made up of English words,
numbers and symbols, with the option the capitalize the beginning of random words,
also known as the XKCD method.

To generate your random password, navigate to the directory containing both the file
"xkcdpwgen" and "words_alpha.txt" (a text file containing all English words). You can
simply call "./xkcdpwgen" to get a random password made up of 4 random all-lowercase
words, or add additional arguments to strengthen the password with capitals, numbers
and symbols:

xkcdpwgen [-h] [-w WORDS] [-c CAPS] [-n NUMBERS] [-s SYMBOLS]

Optional arguments:
-h, --help : show a help message
-w WORDS, --words WORDS : include WORDS words in the password (default = 4)
-c CAPS, --caps CAPS : capitalize the first letter of CAPS random words (default = 0)
-n NUMBERS --numbers NUMBERS : inserts NUMBERS random numbers in the password (default = 0)
-s SYMBOLS, --symbols SYMBOLS : insert SYMBOLS random symbols in the password (default = 0)

Example usage:
"./xkcdpwgen -w 2 --caps 1 --numbers 4 -s 1"
- creates a password with 2 English words (one of which is capitalized), 4 numbers, and 1
symbol all shuffled together. An example might be, "3Pickles9!security67"

"./xkcdpwgen --words 0 -c 10 -n 3 --symbols 2"
- creates a password with 3 numbers and 2 symbols all shuffled together. An example might
be "*4#21"

Thank you to dwyl on Github for creating the words_alpha.txt file used here :)
