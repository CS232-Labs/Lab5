# Champsim Assignment

## Note
* Please note that there is no report this time. All the explanations and reasonings should be presented in a video. You are free to use slides to put information and present it in the video.
* Make sure that every team member is present in the video.

## Part I - Introductory Questions (5 points)
Answer all of the below questions in a video.
- What does the 'handle_fill' function in src/cache.cc do? Explain it in the video.
- The 'handle_fill' function involves a writeback packet. What is the need of the writeback packet? Why can't we modify the cache block directly?
- What is the variable 'fill_level'? What does it store?
- How does champsim get the 'set' and 'way' for a particular address (which functions does it use and what do they do internally)? What is the value of way in case of a cache miss?
- What does the function 'return_data' in src/cache.cc do? Explain its usage.

## Part II - Comparing Cache replacement policies (45 points)
* In this question, we'll be comparing a few basic cache replacment policies like LFU, FIFO and Random Cache replacement policy.

- LFU(__Least frequently used__): Here, we evict the cache line that is least frequently used, where frequency stands for the number of times the cache line is accessed(this could mean both read/write)
- FIFO(__First in First Out__): In this replacement policy, when the cache becomes full we evict the oldest cache block in the set.
- Random: Here we choose a random block to evict in case the cache becomes full.

### Performance Analysis:
We will be comparing the performances(`IPC`, `LLC miss rate`) of these replacement policies for the `Last-level cache` for the following configurations for the provided traces(find them [here](https://drive.google.com/drive/folders/1mxqC5G1D8DshsTo0xGW4Txi1A4v0PcK5)), by changing the number of ways in a set among `1, 4, 16, 32`

Plot the `IPC` and `LLC miss rate` values for different ways mentioned above in a two plots (use a multi-bar chart). Present your reasoning on observations in a video. Which replacement policy works the best? Which works the worst? Give appropriate reasons in your video.

## Part III - Best-Offset hardware prefetching (50 points)
We will be implementing the following paper: https://hal.inria.fr/hal-01165600/document 

* Read the above paper and implement best-offset prefetching. 
* Take the above paper as a baseline and feel free to improve on the paper with your own ideas. Make sure you clearly describe your ideas in the video. 
* There will be a dynamic leader-board based on the performances of different teams and you will get marks accordingly.

## Submission Format
* Submit the compressed champsim folder(the given source + all the changes you make) as `champsim.tar.gz`