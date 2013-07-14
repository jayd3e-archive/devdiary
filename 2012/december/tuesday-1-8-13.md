TODO(once I get back from gym):
* lock comment/solution input, to avoid duplicate submits.
* implement "hide" button that uses the same icon as remove
* shift+enter on create post page should work
* better error reporting
* edit post needs to work with broadcasts

REMARKS:
* For the one-millionth time, Multidict.mixed() returns a nice dictionary, where all
scalar values are left alone, while keys that have more than one value are put into
a list.
* By mixing Multidict.mixed() with the accept_scalar=True kwarg on colander.Schema,
you have a nice recipe for handling every possible input a user will throw at you for
keys that are sequences.