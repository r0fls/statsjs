# statty.js
Statistics for javascript

Intended for `node.js`. Still in development, so to use it currently, you need to clone the repo and put it in your project. Example usage:

    var stats = require('./stats.js')
    console.log(stats.normal(5,1).rand())
    
So far the only distribution is the `normal` distribution, which is initialized with `mean` and `variance`. It then has the following methods:
    
    var stats = require('./stats.js')
    norm = stats.normal(5,1)               \\ normal with mean 5, variance 1
    console.log(norm.pdf(1))               \\ probability density function
    console.log(norm.cdf(4))               \\ cumulative density function
    console.log(norm.quantile(.9))         \\ quantile
    console.log(norm.rand())               \\ generates a random number
    \\or
    norm = stats.normal.fit([1,2,3,4,5])   \\ returns model fitted to data
    console.log(norm.mean)                 \\ mean attribute
    console.log(norm.variance)             \\ variance attribute
