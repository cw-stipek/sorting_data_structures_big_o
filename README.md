# sorting_data_structures_big_o
- The purpose of this notebook is for homework 4 for DSE 511. 
- POC: Clinton Stipek, cstipek@vols.utk.edu
- Please note that my 1-2 page summary is at the bottom of this README

# Objectives
- Implement or call classic sorting algorithms
- Empirically recover big-o growth from runtime experiments
- compare data structure performance on realistic search tasks
- document results with clear code, figures, and interpretation


# Take Aways
How well did your empirical results align with expected big‑O?
What practical advice would you give a teammate choosing data structures and sorting methods?
Were there any surprises in your experiments? Explain.
How did you ensure reproducibility?

One of the biggest takeaways was simply how poor the performance of insertion_sort was in relation to the other algorithms (sorted_builtin, numpy_sort, mergesort, and quicksort). This was very obivous on the plots ('Sorting runtime vs n (linear)'). It was also kind of surprising to see the similarities in runtime for the other sorting algorithms which led me to be a little confused as to why there are so many. I assume that each does things slightly differently and has a following for each one, but they all seem very similar. I am also new to these algorithms so I am also incredibly naive on them. 

My algorithms I plugged in (mergesort, numpy_sort, and quicksort) achieved very similar metrics when compared with sorted_builtin so I was happy they worked well. None of the ones I implemented showed drastically slower time runs. It was interesting to see that when n was 1000 the mergesort and quicksort were quite similar (0.0013 and 0.0010) but when n was 2000 there was quite a difference (0.0027 and 0.00095) and I am not too sure why there is this discrepency. 

I would give my teammate 2-3 different algorithms to test against the insertion_sort to ensure that our approach was outperforming the baseline insertion_sort. I prefer a more explainable one (numpy_sort) which sorts it based on ascending order. From my baseline understanding this is what I would use and it seems to have a high performance in relation to Big-0 as well. I would also recommend they leverage a framework in a dictionary versus a list based on the performance. 

I am incredibly blessed to have access to virtual machines through ORNL which have amazing RAM and core capabilities, but one of my biggest surprises was simply the runtime associated with my script when I did varying sizes and queries for my sorting. It is quite surprising to me to see it running for quite a few hours while waiting for a graph or for the block to be completed. Another interesting find was simply the increased time it took list's to run in relation to a dictionary. 

To ensure reproducible results I am including the rng = np.random.default_rng(seed=13) at the beginning of my script. 