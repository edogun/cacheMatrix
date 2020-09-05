# cacheMatrix
Programming Assignment 2 
makeCacheMatrix <- function(x = matrix()) {
                p <- NULL
                set <- function (y) {
                  x <<- y
                  p <<- NULL
}
  get <- function () x
  setinverse <- function(inverse) p <<- inverse
  getinverse <- function() p
  list(set = set,
       get = get,
       setinverse = setinverse,
       getinverse = getinverse)
}

## to get the value of the inverse

cacheSolve <- function(x, ...) {
  p <- x$getinverse()
    if(!is.NULL(p)){
    message("getting cacheddata")
    return(p)
}
  data <- x$get(
  p <- solve(data,...)
  x$setinverse (p)
  p
} 
 ## Return a matrix that is the inverse
