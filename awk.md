# AWK                                                                                                  #
Based off of "The AWK Programming Language" by Alfred V.Aho, Brian W.Kernighan and Peter J.Weinberger.
This document pretty much works as memory leverage for the information in the book.

---

## 1. An AWK tutorial                                                                                  ##

### 1.1 Getting started                                                                                ###

#### Structure                                                                                         ####

    BEGIN   { action }
    <Selection> { action }
    <Selection> { action }
    ...
    END     { action }


### 1.2 Simple output                                                                                  ###

print


### 1.3 Fancier ouput                                                                                  ###

printf


### 1.4 Selection                                                                                      ###
> Selection patterns can be conbined with logical operators

  - Selection by comparison
  - Selection by computation
> Comparison with computation

  - Selection by text content
> Both regular expressions and plain

  - Selection by keyword
> BEGIN {}
> END {}


### 1.5 Computing with AWK                                                                             ###

length(<var>), NF, NR, ...


### 1.6 Control-Flow Statements                                                                        ###

  1. _if_

        if ( <boolean [expression]> ) {
                <statements>
        } else {
                <statements>
        }


  2. _while_

        position = 1
        while ( position <= $3 ) {
                <statements>
        }


  3. _for_

        for (position = 1; position <= $3; position++) {
                <statements>
        }


  4. _case_

        switch ( <boolean [expression]> ) {
                case <value>: <statements>;break;
                ...
        }


### 1.7 Arrays                                                                                         ###

        <array name>[<element number>]


### 1.8 One-liners                                                                                     ###

        { print $NF }
> Print last field of every line.

        NF > 4
> Print every line with more than 4 fields.

        $NF > 4
> Print every line where the last fields is more than 4.

        { $2 = ""; print }
> Print every line with the second field truncated.



## 2. The AWK language                                                                                 ##

### 2.1 Patterns                                                                                       ###
### 2.2 Actions                                                                                        ###
### 2.3 User-Defined Functions                                                                         ###
### 2.4 Output                                                                                         ###
### 2.5 Input                                                                                          ###
### 2.6 Interaction with other programs                                                                ###

## 3. Data processing                                                                                  ##
## 4. Reports and databases                                                                            ##
## 5. Processing words                                                                                 ##
## 6. Little languages                                                                                 ##
## 7. Experiments with algorithms                                                                      ##
## 8. EPILOG                                                                                           ##