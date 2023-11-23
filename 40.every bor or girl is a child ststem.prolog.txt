child(X) :- boy(X) ; girl(X).
has_toy(X, doll) :- girl(X).
has_toy(X, train) :- child(X), \+ boy(X).
has_toy(X, lump_of_coal) :- child(X), \+ has_good_behavior(X).

boy(jack).

has_good_behavior(jack).

girl(emma).


##
true .

?- has_toy(jack, Toy).
false.

?- has_toy(susan, Toy).
false.

?- boy(susan).
false.

?- has_good_behavior(jack).
true.

?- has_toy(emma, lump_of_coal).
true.

?-  has_toy(susan, Toy).
false.
