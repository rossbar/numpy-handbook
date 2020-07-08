% Outline for chapter on numpy arrays
%
% Probably chapter 1

% TODO: Better title
# The `ndarray` data structure

% TODO: This question maybe better in a preface?
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
 - [The `ndarray` page][numpyref-ndarray] in the NumPy reference guide
 - [The NumPy internals page][numpyref-internals] in the NumPy reference guide
 - [Life of `ndarray`][sln-anatomy] chapter in the scipy lecture notes

[numpyref-ndarray]: https://numpy.org/doc/stable/reference/arrays.ndarray.html
[numpyref-internals]: https://numpy.org/doc/stable/reference/internals.html#internal-organization-of-numpy-arrays
[sln-anatomy]: https://scipy-lectures.org/advanced/advanced_numpy/index.html#life-of-ndarray


### Terminology

 - single-segment vs. contiguous vs. C-contiguous/F-contiguous
   * Examples of *single-segment* arrays that are neither C or F 
     contiguous (higher dims)
     - Corollary: high dimensional arrays that are *both* C and F contiguous?
       * Yes! dims == 1 (sort of a trick question)
   * Can create non-contiguous arrays with views (`[::2]`)
   * Statement whose truth value needs to be confirmed, but is a useful 
     distillation of some of the terminology into a more concrete example:
    
     > In NumPy, it is not possible to construct a **non-single-segment** 
     > array that is not a **view** of a single-segment array.
 - Terminological aside: memory *contiguity* vs. memory *alignment*

### Views

 - Expand on the classic example of `transpose`
