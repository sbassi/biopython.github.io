---
title: GSOC2011 Mocapy
permalink: wiki/GSOC2011_Mocapy
layout: wiki
---

Mocapy++ is a machine learning toolkit for training and using Bayesian
networks. It has been used to develop probabilistic models of
biomolecular structures. The goal of this project is to develop a Python
interface to Mocapy++ and integrate it with Biopython. This will allow
the training of a probabilistic model using data extracted from a
database. The integration of Mocapy++ with Biopython will provide a
strong support for the field of protein structure prediction, design and
simulation.

Introduction
------------

Discovering the structure of biomolecules is one of the biggest problems
in biology. Given an amino acid or base sequence, what is the three
dimensional structure? One approach to biomolecular structure prediction
is the construction of probabilistic models. A Bayesian network is a
probabilistic model composed of a set of variables and their joint
probability distribution, represented as a directed acyclic graph. A
dynamic Bayesian network is a Bayesian network that represents sequences
of variables. These sequences can be time-series or sequences of
symbols, such as protein sequences. Directional statistics is concerned
mainly with observations which are unit vectors in the plane or in
three-dimensional space. The sample space is typically a circle or a
sphere. There must be special directional methods which take into
account the structure of the sample spaces. The union of graphical
models and directional statistics allows the development of
probabilistic models of biomolecular structures. Through the use of
dynamic Bayesian networks with directional output it becomes possible to
construct a joint probability distribution over sequence and structure.
Biomolecular structures can be represented in a geometrically natural,
continuous space. Mocapy++ is an open source toolkit for inference and
learning using dynamic Bayesian networks that provides support for
directional statistics. Mocapy++ is excellent for constructing
probabilistic models of biomolecular structures; it has been used to
develop models of protein and RNA structure in atomic detail. Mocapy++
is used in several high-impact publications, and will form the core of
the molecular modeling package Phaistos, which will be released soon.
The goal of this project is to develop a highly useful Python interface
to Mocapy++, and to integrate that interface with the Biopython project.
Through the Bio.PDB module, Biopython provides excellent functionality
for data mining biomolecular structure databases. Integrating Mocapy++
and Biopython will allow training a probabilistic model using data
extracted from a database. Integrating Mocapy++ with Biopython will
create a powerful toolkit for researchers to quickly implement and test
new ideas, try a variety of approaches and refine their methods. It will
provide strong support for the field of biomolecular structure
prediction, design, and simulation.

Author & Mentors
----------------

[Michele Silva](User%3AMchelem "wikilink") michele.silva@gmail.com

**Mentors**

  
Thomas Hamelryck

Eric Talevich

Project Schedule
----------------

### Work Plan

'''Gain understanding of SEM and directional statistics '''

-   Review the theory behind machine learning for bioinformatics, Markov
    chain Monte Carlo and dynamic Bayesian networks.

<!-- -->

-   Build the theoretical background on the algorithms used in Mocapy++,
    such as parameter learning of Bayesian networks using Stochastic
    Expectation Maximization (SEM).

'''Study Mocapy++'s use cases '''

-   Read several papers and attempt to replicate part of the experiments
    described using Mocapy++.

<!-- -->

-   Get a better understanding of biological sequence analysis done
    through probabilistic models of proteins and nucleic acids.

'''Work with Mocapy++ '''

-   Understand Mocapy++'s internal architecture and algorithms by
    exploring its source code and running its test cases.

<!-- -->

-   Research other applications of Mocapy++ in Bioinformatics.

'''Design Mocapy++'s Python interface '''

-   Explore the source code of Biopython to understand its design
    and implementation. The Mocapy++ interface to be included in
    Biopython must be made compatible with the methods of solving
    problems in Biopython.

<!-- -->

-   Design a Python interface for Mocapy++, based on its data structures
    and algorithms. Examine Mocapy++'s use cases and existing test cases
    to provide guidance for the interface design.

'''Implement Python bindings '''

-   Implement test cases in Python using the new interface to Mocapy++.

<!-- -->

-   Implement python bindings for the defined interface.

'''Explore Mocapy++'s applications '''

-   Develop example applications that involve data mining of
    biomolecular structure databases using Biopython.

<!-- -->

-   Formulate probabilistic models using Python-Mocapy++. Apply the
    models to solve biological problems. Examples of problems that can
    be solved using dynamic Bayesian networks include deciding if a pair
    of sequences is evolutionarily related, finding sequences which are
    homologous to a known evolutionary family and predicting RNA
    secondary structure.

### Timeline

''Before April 25 ''

-   Get involved with the Biopython project and community.

<!-- -->

-   Learn the statistical methods used in Mocapy++ and relevant concepts
    in structural biology.

'''Community bonding period '''

''April 25 - May 22 (4 weeks) ''

-   Familiarize myself with Mocapy++'s functionality and architecture.

<!-- -->

-   Configure a development environment and explore the Mocapy++ and
    Bio.PDB source code more thoroughly. Document the code
    during exploration.

<!-- -->

-   Study Mocapy++ and Bio.PDB test cases in order to understand the
    Mocapy++ interface requirements.

<!-- -->

-   Compare options to create python bindings to C++ code (Boost Python,
    Cython, Swig). Perform the necessary assesments and gathering of
    requirements to determine the best library to create the
    Python bindings.

<!-- -->

-   Try fixing bugs in Biopython in order to get familiar with the
    development cycle.

'''Begin of coding phase '''

''May 23 - June 5 (2 weeks) ''

-   Design and implement test cases for the Mocapy++ Python interface.
    The tests must include data structures such as the Multi-Dimentional
    array; and statistic models such as the hidden Markov Models, a
    special case of dynamic Bayesian networks.

<!-- -->

-   Identify functions and data structures which impose challenges for
    the creation of Python bindings.

<!-- -->

-   Implement Python bindings for the core functions and data
    structures, especially the ones which are straightforward to wrap.

''June 6 - June 19 (2 weeks) ''

-   Implement Python bindings for the remaining Mocapy++ functionality
    that composes its interface.

<!-- -->

-   Run and improve the previously designed test cases. Make sure the
    newly designed interface meets the requirements of the use cases.

<!-- -->

-   Do performance analysis (code profiling) in order to make sure the
    Python interface of Mocapy++ is fast enough to be usable.

<!-- -->

-   Try other options to create Python bindings to C++ code, in case the
    implementation doesn't meet the speed requirements.

''June 20 - July 3 (2 weeks) ''

-   Integrate the Mocapy++ Python interface with Biopython.

<!-- -->

-   Implement integration tests for Mocapy++ Biopython.

<!-- -->

-   Test the operation of each module of the modified source code.

''June 4 - July 10 (1 week) ''

-   Make further changes in the code to improve robustness
    and functionality.

<!-- -->

-   Gather, organize, and improve the documentation written during the
    previous weeks.

Mid-term evaluations (July 11)

''July 11 - July 24 (2 weeks) ''

-   Design probabilistic models for biological problems. Solve them
    using Mocapy++ Biopython.

<!-- -->

-   Offer the code to the community for testing and suggestions for
    further functionality.

''July 25 - August 7 (2 weeks) ''

-   Create applications which use the data mining provided by Bio.PDB
    together with the machine learning features of Mocapy++.

<!-- -->

-   Profile the code and work on speed and robustness improvements.

''August 8 - August 14 (1 week) ''

-   Perform last review and improvements on code and documentation.

''August 15 - August 21 (1 week) ''

-   A buffer for any unpredictable delay.

'''Firm pencils down (August 22) '''

Project Code
------------

Hosted at [the gSoC11 Mocapy
branch](http://mocapy.svn.sourceforge.net/viewvc/mocapy/branches/gSoC11/)

Project Progress
----------------

### Options to create Python bindings to C++ code

#### Swig

There is already an effort to provide bindings for Mocapy++ using Swig.
However, Swig is not the best option if performance is to be required.
The Sage project aims at providing an open source alternative to
Mathematica or Maple. Cython was developed in conjunction with Sage (it
is an independent project, though), thus it is based on Sage's
requirements. They tried Swig, but declined it for performance issues.
According to the [Sage programming
guide](http://sage.math.washington.edu/tmp/sage-2.8.12.alpha0/doc/prog/node36.html)
"The idea was to write code in C++ for SAGE that needed to be fast, then
wrap it in SWIG. This ground to a halt, because the result was not
sufficiently fast. First, there is overhead when writing code in C++ in
the first place. Second, SWIG generates several layers of code between
Python and the code that does the actual work". This was written back in
2004, but it seems things didn't evolve much. The only reason I would
consider Swig is for future including Mocapy++ bindings on BioJava and
BioRuby projects.

#### Boost Python

Boost Python is comprehensive and well accepted by the Python community.
I would go for it for its extensive use and testing. I would decline it
for being hard to debug and having a complicated building system. I
don't think it would be worth including a boost dependency just for the
sake of creating the Python bindings, but since Mocapy++ already depends
on Boost, using it becomes a more attractive option. In my personal
experience, Boost Python is very mature and there are no limitations on
what one can do with it. When it comes to performance, Cython still
overcomes it. Have a look at the [Cython C++ wrapping
benchmarks](http://blog.behnel.de/index.php?p=38) and check the timings
of [Cython against Boost Python](http://www.behnel.de/cycppbench/).
There are also previous [benchmarks comparing Swig and Boost
Python](http://telecom.inescporto.pt/~gjc/pybindgen-benchmarks/).

#### Cython

It is incredibly faster than other options to create python bindings to
C++ code, according to several benchmarks available on the web. Check
the Simple benchmark between Cython and Boost.Python. It is also very
clean and simple, yet powerful. Python's doc on porting extension
modules mentions cython: "If you are writing a new extension module, you
might consider Cython." Cython has now support for efficient interaction
with numpy arrays. it is a young, but developing language and I would
definitely give it a try for its leanness and speed.

Since Boost is well supported and Mocapy++ already relies on it, we
decided to use Boost.Python for the bindings.

For further information see [Mocapy++Biopython - Box of
ideas](https://docs.google.com/document/d/1E72Qysp3pMd69hSYfIXJKgBLdeSMbzSol9RYD2rKHlI/edit?hl=pt_BR&authkey=CPmFxK0H).

### Bindings Prototype

The source code for the prototype is on the gSoC11 branch:
<http://mocapy.svn.sourceforge.net/viewvc/mocapy/branches/gSoC11/bindings_prototype/>

Bindings for a few Mocapy++ features and a couple of examples to find
possible implementation and performance issues.

**Procedure**

-   Implemented the examples hmm\_discrete and
    discrete\_hmm\_with\_prior in Python, assuming the interface
    Mocapy++ already provides.

<!-- -->

-   Implemented the bindings to provide a minimum subset of
    functionality, in order to run the implemented examples.

<!-- -->

-   Compared the performance of C++ and Python versions.

Mocapy++’s interface remained unchanged, so the tests look similar to
the ones in Mocapy/examples.

In the prototype the bindings were all implemented in a single module.
For the actual implementation, we could mirror the src packages
structure, having separated bindings for each package such as discrete,
inference, etc.

It was possible to implement all the functionality required to run the
examples. It was not possible to use the
[vector\_indexing\_suite](http://www.boost.org/doc/libs/1_42_0/libs/python/doc/v2/indexing.html)
when creating bindings for vectors of MDArrays. A few operators (in the
MDArray) must be implemented in order to export indexable C++ containers
to Python.

Two Mocapy++ examples that use discrete nodes were implemented in
Python. There was no problem in exposing Mocapy’s data structures and
algorithms. The performance of the Python version is very close to the
original Mocapy++.

For additional details have a look at the [Mocapy++ Bindings
Prototype](https://docs.google.com/document/d/1JPkCbvJ9Gk3b6LmQ68__UUt4Yz2P1-c286p6FVEqyXs/edit?hl=pt_BR&authkey=CJTCpZgL)
report.

### Bindings Implementation

*May 23 - Jun 5: Bindings for the core functions and data structures*

''' Data structures '''

Mocapy uses an internal data structure to represent arrays: MDArray. In
order to make it easier for the user to interact with Mocapy's API, it
was decided to provide an interface that accepts numpy arrays.
Therefore, it was necessary to implement a translation between a numpy
array and an MDArray.

The translation from MDArray to python was done through the use of
Boost.Python
[to\_python\_converter](http://www.boost.org/doc/libs/1_43_0/libs/python/doc/v2/to_python_converter.html).
We've implemented a template method convert\_MDArray\_to\_numpy\_array,
which converts an MDArray of any basic type to a corresponding numpy
array. In order to perform the translation the original array's shape
and internal data are copied into a new numpy array.

The numpy array was created using the [Numpy Array
API](http://docs.scipy.org/doc/numpy/reference/c-api.array.html). The
creation of a new
[PyArrayObject](http://docs.scipy.org/doc/numpy/reference/c-api.types-and-structures.html#PyArrayObject)
using existing data (PyArray\_SimpleNewFromData) doesn't copy the array
data, it just stores a pointer to it. Thus, one can only free the data
when there is no reference to the object. This was done through the use
of a [Capsule](http://docs.python.org/c-api/capsule.html). Besides
encapsulating the data, the capsule also stores a destructor to be used
when the array is destroyed. The PyArrayObject has a field named "base"
which points to the capsule.

The translation from Python to C++, i.e. creating an MDArray from a
numpy array is slightly more complex. Boost.Python will provide a chunk
of memory into which the new C++ object must constructed in-place. See
the [How to write boost.python
converters](http://misspent.wordpress.com/2009/09/27/how-to-write-boost-python-converters/)
article for more details.

A translation between std::vector of basic types (double, int...) and
Python list was also implemented. For std::vector of custom types, such
as Node, the translation to a Python list was not performed. If done the
same ways as for basic types, a type error is raised: "TypeError: No
to\_python (by-value) converter found for C++ type". When using
[vector\_indexing\_suite](http://www.boost.org/doc/libs/1_46_1/libs/python/doc/v2/indexing.html#vector_indexing_suite_class)
this problem was already solved. See [Wrapping
std::vector<AbstractClass*>](http://mail.python.org/pipermail/cplusplus-sig/2005-July/008865.html).
The only inconvenience of using the vector\_indexing\_suite is creating
new types such as vector\_Node, instead of using a standard Python list.

The code for the translations is in the
[mocapy\_data\_structures](http://mocapy.svn.sourceforge.net/viewvc/mocapy/branches/gSoC11/bindings/mocapy_data_structures.cpp?revision=340&view=markup)
module.

''' Core functions '''

The mocapy Python packages follow Mocapy's current source tree. For each
package, a shared library with the bindings was created. This makes
compilation faster and debug easier. Also, if a single library was
created it wouldn't be possible to define packages.

Each of the libraries is called libmocapy\_<nameofthepackage>. For
example, libmocapy\_gaussian provides bindings for the gaussian nodes
and probability distributions. The libmocapy\_data\_structures is used
by other libraries and, therefore, must be imported first. This is done
on the Python side. Each of the libmocapy\_\* libraries is imported in
the corresponding package. See [Creating
Packages](http://www.boost.org/doc/libs/1_46_1/libs/python/doc/tutorial/doc/html/python/techniques.html#python.creating_packages).

The bindings code can be found in the [Bindings
directory](http://mocapy.svn.sourceforge.net/viewvc/mocapy/branches/gSoC11/bindings/).

Currently, tests to the just created interface are being developed.
There are a few tests already implemented under the framework package:
[mocapy/framework/tests](http://mocapy.svn.sourceforge.net/viewvc/mocapy/branches/gSoC11/python/mocapy/framework/tests/)