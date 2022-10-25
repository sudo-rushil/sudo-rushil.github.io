---
layout: default
---

# Rushil Mallarapu

_publications, projects, and ponderings_

I'm Rushil Mallarapu

I am a second-year in the Harvard class of '25.

Here you can find a list of publications I've worked on, a selection of projects I did, my thoughts on different things I'm working on, and more!

You might know me from

- Fairfield Ludlowe Rocketry Team
- Southport Enrichment Club
- The Rovis Lab at Columbia University
- Research Mentorship Program (2019 and 2020) at the University of California, Santa Barbara

Please feel free to contact me through any of the mediums to the left. The easiest way is definitely through emailing me at [rushil_mallarapu@college.harvard.edu](mailto:rushil_mallarapu@college.harvard.edu).

```haskell
-- The elegant quicksort no one told you about

quicksort :: Ord a => [a] -> [a]
quicksort []      = []
quicksort [x]     = [x]
quicksort (x:xs)  
    = quicksort (filter (<x) xs) ++ [x] ++ quicksort (filter (>x) xs)
```
