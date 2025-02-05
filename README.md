# go-duckdb-dependencies

Repo to test / play around with ways to provide pre-built dependencies.

To use:
Import both dependencies.
```
import (
// ...
	_ "github.com/marcboeker/go-duckdb"
	_ "github.com/taniabogatsch/go-duckdb-dependencies/macos-arm64"
)
```
Build your project with
```
CGO_LDFLAGS="-lc++ -lduckdb -L/$GOPATH/pkg/mod/github.com/taniabogatsch/go-duckdb-dependencies/macos-arm64@v0.1.3/" go build -tags=duckdb_use_static_lib
```
