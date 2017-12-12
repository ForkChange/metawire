# metawire

BitTorrent Extension for Peers to Fetch Metadata Files (BEP 9)

# Install
```bash
go get github.com/fanpei91/metawire
```

# Uasge
```go
import "github.com/fanpei91/metawire"
```

# API

```go
var (
	ErrExtHeader    = errors.New("metawire: invalid extention header response")
	ErrInvalidPiece = errors.New("metawire: invalid piece response")
	ErrTimeout      = errors.New("metawire: time out")
)
```

#### func  Timeout

```go
func Timeout(t time.Duration) option
```

#### type Wire

```go
type Wire struct {
}
```


#### func  New

```go
func New(infohash string, from string, options ...option) *Wire
```

#### func (*Wire) Fetch

```go
func (w *Wire) Fetch() ([]byte, error)
```
