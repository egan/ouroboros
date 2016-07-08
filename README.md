# ouroboros
Ouroboros will be a Python library for general systems analysis in the Karnopp bond graph framework.

I am not a software engineer so bear with me as I try to develop a workable architecture.

## Scope
1. Generalized Models:
	* Provide an object that can be passed to a suitable integrator for time domain simulation.
	  This object will encapsulate generalized relationships so that nonlinear constitutive laws and modulated 2-ports may be implemented.
	* Check the validity of signal flow graph.
	* Keep LTI models compatible with linear analysis tools (SciPy).
2. Bond Graph Representation:
	* Provide a mechanism to represent bond graphs easily, including signal flows.
	* Check the validity of bond graphs.
	* Save and load bond graphs.
	* Output bond graphs in graphical format (e.g. TikZ)?
3. Bond Graph Transformation:
	* Provide methods to simplify bond graphs.
	* Perform automatic causal assignment procedure.
	* Provide methods to develop models from bond graphs, handling algebraic loops, nonlinear constitutive laws, and modulated 2-ports.
4. Elements:
	* Provide an object that represents bond graph elements.
	* In addition to classical linear elements, include a small library of useful nonlinear elements.

The library should fit in with the SciPy toolset, using NumPy types and probably SymPy.
Additionally, the library should be units-aware and be compatible with Pint.

## About
See the [poor] article on [Wikipedia](https://en.wikipedia.org/wiki/Bond_graph) for an overview of what bond graphs are.
This library is intended not only to represent bond graphs but also to make it easy to use the analysis framework promoted by professor Dean Karnopp of UC Davis in his courses there and in his book [System Dynamics: Modeling, Simulation, and Control of Mechatronic Systems](https://www.amazon.com/System-Dynamics-Modeling-Simulation-Mechatronic/dp/047088908X).

About the name:
Prof. Karnopp tells a story about how Kerkulé realized the molecular structure of benzene by seeing an ouroboros in a daydream.
He points out that the bond graph of a Wheatstone bridge can be structured similar to benzene and explains that this was Henry Paynter's inspiration to call it "bond graph".
This being a Python project, a snake-related name seemed appropriate.
