This is a reproducible example for:
https://github.com/golang/go/issues/27706

The repository contains three docker files for the three examples provided at the issue above. To run the examples:

### 1. `go get` without go.mod (success)
```
docker build . -f Dockerfile-1 -t go-issue-27706-1
```

### 2. `go get` with go.mod (failure)
```
docker build . -f Dockerfile-2 -t go-issue-27706-2
```

### 3. `CGO_ENABLED=0 go get` with `go.mod` (success)
```
docker build . -f Dockerfile-3 -t go-issue-27706-3
```
