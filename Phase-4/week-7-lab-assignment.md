Warm-up for Phase 4.

Implement Phase 4's query-side logic single-threaded. Reuse the Phase 4 trace parser; this warm-up just walks the records in order on one thread:

- **ADD**: append the edge to the graph; push `src` into a `pending_dirty` vector.
- **Q**: run incremental SSSP: a push-style BSP starting from the deduplicated `pending_dirty`, updating the persistent `dist[]` in place. Then clear `pending_dirty`.
- **D**: ignore.

Seed `pending_dirty` with `{source}` at startup so the first Q's frontier contains the source vertex.

**Test.** Use the signature output and verification from Phase 4's *Testing & Verification*.

Please submit your code (copy/paste the implementation) and execution result on Canvas.