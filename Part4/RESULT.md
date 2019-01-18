
Part 4 Results

The expected output from this calculation is 0, since we decrement i just as many times as we increment i. However, due to the incrementation operation happening over multiple steps, we have a race condition, resulting in strange answers The magic number rarely equal 0.

Both C and python uses threads, which causes this to happen.

Go uses coroutines (goroutines) which is similar to threads, but not exactly. However, the same results appear here.
