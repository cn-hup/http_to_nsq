# http_to_nsq

 Publishes HTTP requests to NSQD.

## About

 Useful for things like creating an end-point for CI web hooks.

 Currently only JSON bodies are supported, this may be converted to a blob later, but base64 is meh, so for now JSON is it!

## Usage

#### type Message

```go
type Message struct {
  URL    string                 `json:"url"`
  Method string                 `json:"method"`
  Header http.Header            `json:"header"`
  Body   map[string]interface{} `json:"body"`
}
```

# License

MIT