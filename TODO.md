# Individual-based models of cultural evolution TO DO

### Suggestions:

from [@ed_hagen](https://twitter.com/ed_hagen/status/1333547688223072256):
Consider adding section on parallel processing. I've tripled the speed of my R-based simulations on my 4-core machine with this simple code:

```r
library(furrr)
plan('multisession')
results <- future_pmap_dfr(
  param_grid, ~simulate(10000, ...), 
  .id='param_set'
)
```

--
