% Outline for chapter on numpy arrays
%
% Probably chapter 1

% TODO: Better title
# The `ndarray`

What's the motivation for learning about NumPy arrays?
 - *De facto* data exchange object for the scientific Python ecosystem
 - Excuse to drop in some cool examples (EHT, LIGO, etc.)
 - ASIDE: scientific Python ecosystem
   * NumPy doesn't exist in a vacuum - it provides one important building block
     for the scientific Python ecosystem.
     The book will use components from related libraries, but the primary 
     focus is NumPy
   * Include ecosystem image from NumPy paper
   * Aliases: scipy ecosystem/stack 

Incredibly flexible, generic n-dimensional array data structure with powerful
features
 - Concise, expressive syntax for full-featured data access (indexing)

Combines with additional machinery provided by numpy for operating on array
data:
 % TODO: Add forward xrefs to relevant sections/chapters
 - Built-in, array-aware operations (`ufuncs`)
 - *Broadcasting*
 - *Vectorization*

## A closer look at `ndarray`

Related:
 - [Life of `ndarray`][sln-anatomy] chapter in the scipy lecture notes

[sln-anatomy]: https://scipy-lectures.org/advanced/advanced_numpy/index.html#life-of-ndarray
