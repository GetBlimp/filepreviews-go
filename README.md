# Filepreviews-Go
This is a client library for the **Demo API** of [FilePreviews.io](http://filepreviews.io) service. A lot more to come very soon.

[Sign up to beta](http://eepurl.com/To0U1)

## Installation
```bash
$ go get github.com/elbuo8/filepreviews-go
```

### Example code
```go
fp := New()
opts := &FilePreviewsOptions{}
_, err := fp.Generate("http://www.getblimp.com/images/screenshot1.png", opts)
```

#### Options
You can optinally send an options object.
```go
fp := New()
opts := &FilePreviewsOptions{
	Size: map[string]int{
		"width":  50,
		"height": 100,
	},
	Metadata: []string{"all"},
}
_, err := fp.Generate("http://www.getblimp.com/images/screenshot1.png", opts)
```

## CLI Tool

### Installation
```bash
$ go install github.com/elbuo8/filepreviews-go/filepreviews
```

### Usage
```bash
$ filepreviews -url=https://www.filepicker.io/api/file/0ehaqJwCTSq4P6jMrix6
```

## MIT
