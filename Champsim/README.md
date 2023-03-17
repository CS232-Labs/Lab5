# Champsim Assignment 

## Part I - Introductory Questions

## Part II - Comparing Cache replacement policies
* In this question, we'll be comparing a few basic cache replacment policies like LFU, FIFO and Random Cache replacement policy.

- LFU(__Least frequently used__): Here, we evict the cache line that is least frequently used, where frequency stands for the number of times the cache line is accessed(this could mean both read/write)
- FIFO(__First in First Out__): In this replacement policy, when the cache becomes full we evict the oldest cache block in the set.
- Random: Here we choose a random block to evict in case the cache becomes full.

### Performance Analysis:
We will be comparing the performances(`IPC`) of these replacement policies for the `Last-level cache` for the following configurations for the provided traces(inside `Champsim/traces`), by changing the number of ways in a set among `1, 4, 16, 32`

Plot the IPC values for different ways mentioned above in a single plot (use a multi-bar chart). Present your reasoning on observations in a video. Which replacement policy works the best? Which works the worst? Give appropriate reasons in your video.

### Part III - Best-Offset hardware prefetching
