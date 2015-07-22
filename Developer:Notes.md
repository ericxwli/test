### Avoiding dead-locks

A common dead-lock scenario is:

Thread 1 acquires `Lock A` and then waits for `Lock B`.
Meanwhile, Thread 2 acquires `Lock B` and waits for `Lock A`.

In the browser, this manifests typically as a contention between `tree-lock` and an element of the DOM tree.

To avoid the deadlock, we are following a priority based approach:

* If a thread only requires one of the locks, it can take it directly.
* If a thread needs both tree-lock and an element lock, then the tree-lock should be acquired first, and then while holding it, the element lock should be taken.