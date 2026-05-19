Replace the `std::thread`-based parallel runner from Phase 2a with an OpenMP-based runner. The `BspAlgorithm` interface and the BFS algorithm itself are unchanged; only the runner changes.

Implement a new runner `BspParallelOmp(g, algo, nthreads)` that parallelizes the vertex loop inside each round with OpenMP, and test it under two scheduling modes:

- **Static batch**: `#pragma omp parallel for schedule(static)`. Each thread is preassigned a contiguous block of vertices at loop entry.
- **Dynamic**: `#pragma omp parallel for schedule(dynamic, chunk)`. Chunks sit in a shared queue; each thread grabs the next chunk when it finishes its current one, so faster threads naturally end up processing more chunks than slower threads.

Useful API: `omp_set_num_threads(n)` to set the thread count, and `omp_get_thread_num()` to obtain `tid` for `Process(tid, v, g)`.

Run **BFS only** on `soc-LiveJournal1-weighted.txt` with `source = 0` and `nthreads = 4` three times, all on the same machine: your Phase 2a `std::thread` parallel BFS, OpenMP `schedule(static)`, and OpenMP `schedule(dynamic)`. Measure the execution time of each run.

Please submit your code (copy/paste the OpenMP runner and the three invocations) and the execution result on Canvas. The image must clearly print all three measured times in the following format:

```
BFS (std::thread):    time = <ms>
BFS (OpenMP static):  time = <ms>
BFS (OpenMP dynamic): time = <ms>
```

Also include a short answer in your submission: **which one is faster, and why?**