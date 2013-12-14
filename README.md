# Synopsis

    :- use_module(library(quickcheck)).

    % reversing a list twice gives back the same list
    prop_reverse_twice(L:list) :-
        reverse(L, R),
        reverse(R, L).

    ?- quickcheck(prop_reverse_twice/1).
    % 100 tests OK
    true.
    

# Description

Randomized testing of program properties in the spirit of [QuickCheck](http://hackage.haskell.org/package/QuickCheck).  Describe properties of your predicates and let `library(quickheck)` generates test cases for you.

# Changes in this Version

  * Initial public release

# Installation

Using SWI-Prolog 6.3 or later:

    ?- pack_install(quickcheck).

This module uses [semantic versioning](http://semver.org/).

Source code available and pull requests accepted at
http://github.com/mndrix/quickcheck

@author Michael Hendricks <michael@ndrix.org>
@license BSD
