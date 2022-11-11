# roundm
V3.00

*** Currently in testing phase; all modules ***
- Release estimated at 1 Jan 2023

#
#DESCRIPTION

Roundm is an 'interactive' bash script that performs rounding on numerical values of input file. The significance is to be specified by the user. The current version creates intermediate text files of all steps for validation purposes. 

There are various rounding modules to choose from. With the different rounding modules, user is able to specify whether to perform rounding up or down to nearest (multiple of) specified decimals (e.g. 0.05, or 0.00500129), or to nearest (multiple of) specified full number (e.g. 1.05, 100.00, or 2004.50, etc.). User can of course also choose to have full_number rounded to nearest specified significance.

Free to use and edit by all, for the obvious reason.

glhf

#
#ROUNDING DOWN MODULES

- v1.01 Rounds down to the nearest (multiple of) specified decimals with the integer as starting point (e.g. with rounding down set at 0.75, the number 1,55 will round down to 1.00)

- v1.02 Rounds down to the nearest (multiple of) specified decimals with 0 (zero) as starting point (e.g. with rounding down set at 0.75, the number 1,55 will round down to 1.50)

- v1.03 Rounds down to the nearest (multiple of) specified decimals with starting point to be specified by user (e.g. with rounding down set at  0.05 and starting point set at 2.31, the number 3.99 will round down to 3.96).

- v1.04 Rounds down to nearest (multiple of) specified full number with starting point NEXT_GREATER_NUMBER (e.g. with rounding down set at 21 and full_number 53646.24, NEXT_GREATER_NUMBER will be 53600, resulting in rounded down number 53642)

- v1.05 Rounds down to the nearest (multiple of) specified full number with 0 (zero) as starting point (e.g. with rounding down set at 21, the number 53646.24 will round down to 53634)

- v1.06 Rounds down to the nearest (multiple of) specified full number with starting point to be specified by user (e.g. with rounding down set at  1.05 and starting point set at 2.31, the number 3.37 will round down to 3.36).

#
#ROUNDING UP MODULES

- v1.01 Rounds up to the nearest (multiple of) specified decimals with the integer as starting point (e.g. with rounding up set at 0.75, the number 1,55 will round up to 1.75)

- v1.02 Rounds up to the nearest (multiple of) specified decimals with 0 (zero) as starting point (e.g. with rounding up set at 0.75, the number 1,55 will round up to 2,25)

- v1.03 Rounds up to the nearest (multiple of) specified decimals with starting point to be specified by user (e.g. with rounding up set at  0.05 and starting point set at 2.31, the number 2.37 will round up to 2.41).

- v1.04 Rounds up to nearest (multiple of) specified full number with starting point NEXT_GREATER_NUMBER (e.g. with rounding up set at 21, the number 53646.24 will round up to 53663)

- v1.05 Rounds up to the nearest (multiple of) specified full number with 0 (zero) as starting point (e.g. with rounding up set at 21, the number 53646.24 will round up to 53655)

- v1.06 Rounds up to the nearest (multiple of) specified full number with starting point to be specified by user (e.g. with rounding up set at  1.05 and starting point set at 2.31, the number 2.37 will round up to 4.41).


#
#MECHANISM

The rounding mechanism is simple. It uses only basic math (if one could even call it that) and non-complex scripting. Roundm can therefore be 'recreated' in basically any language without the use of complex code/scripts, provided that some sort of basic calc function is available.


- for rounding to (multiple of) specified decimals:

Of the original number, the decimals are divided by the specified significance, which results in a multiplication factor. If the multiplication factor is not a whole number, for rounding down is taken the integer, and for rounding up the integer plus one (+1). The specified significance is then multiplied by the multiplication factor, which is then added to the original's number integer, resulting in a new full number that is rounded up or down to the specifications of the user.

- for rounding to (multiple of) specified full number (e.g. rounding up to nearest 22.23):

Of the original number, the full number is divided by the specified significance, which results in a multiplication factor. If the multiplication factor is not a whole number, for rounding down is taken the integer, and for rounding up the integer plus one (+1). The specified significance is then multiplied by the multiplication factor, which results in a new full number that is rounded up or down to the specifications of the user.

#
After input file, rounding module, and significance are specified by user, roundm will apply the selected method of rounding to all numbers of input file. Output is logged in new text file to be named by user. Roundm accepts both comma and dot as separator of the integer and decimals. Standard output will be with dot as separator, but user can specify this to be comma as well.

#
#FORMATS

Roundm works with the following list/file format:

- One numerical value per line
- Any amount of lines
- Integer separated from decimal(s) by either dot or comma
- The input file can contain text or symbols or spaces on lines, but the output will be incorrect for that line
- The only symbol that is accepted by roundm and which provides accurate output is the symbol - to mark a negative number (e.g. -23.48373, but not - 23.48373)

#
#FORMULAS

Roundm applies the following formulas for rounding:

ROUNDING DOWN MODULES

- v1.01  ...
- v1.02 ...
- v1.03 ...
- v1.04 ...
- v1.05 ...
- v1.06 ...

ROUNDING UP MODULES

- v1.01 ...
- v1.02 ...
- v1.03 ...
- v1.04 ...
- v1.05 ...
- v1.06 ...


#
#Missing an option? Do tell, so that it will be included.
