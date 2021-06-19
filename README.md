# Execution Context

Responsible to make work available and to get work performed. It binds together work that needs to be done with the computational power required to get it done.

Execution contexts must, however, take into consideration the synchronization context of each work item in order to guarantee that work in the same synchronization context must never run concurrently.

# Synchronization Context

A property of work items that ensure work tagged with the same synchronization context will be properly serialized for execution.

# Work

Some function that needs to be given some data and executed in a particular execution context; such execution, however, must comply to the synchronization context requirement.

# Post

To post work to an execution context means to engage the computational power available to the execution context into executing this work.

It also means that this given particular work instance *must be executed precisely by the required execution context* &mdash; if there are any previous work in the same synchronization context being processed (or waiting to be processed) by some other execution context, the execution context currently being posted must start buffering all work in the same synchronization context until there are no more such previous work left in other contexts.

Also, even if attached to the same execution context, work in the same synchronization context must not run concurrently.
