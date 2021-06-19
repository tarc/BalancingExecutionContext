# Execution Context

Responsible to make work available and to get work performed. It binds together work that needs to be done with the computational power required to do it.

# Work

Some function that needs to be given some data and executed in a particular context.

There must be some equivalence relation between work items grouping in the same equivalence class all work that must not be executed concurrently.

# Post

To post work to an execution context means to engage the computational power available to the context into executing this work.

It also means that that given particular work instance *must be executed precisely by the required execution context* &mdash; if there are any previous work in the same equivalence class being processed (or waiting to be processed) by some other execution context, the execution context currently being posted must start buffering all work pertaining to this class until there are no more previous work left in other contexts.
