[![Build Status](https://travis-ci.com/philips-software/go-hsdp-signer.svg?branch=master)](https://travis-ci.com/philips-software/go-hsdp-signer) [![Slack](https://philips-software-slackin.now.sh/badge.svg)](https://philips-software-slackin.now.sh)
[![Slack](https://philips-software-slackin.now.sh/badge.svg)](https://philips-software-slackin.now.sh)

# Go HSDP Signer

This package implements the HSDP API signing algorithm.
You can sign a http.Request instances 

## Usage

```go

import (
  "github.com/philips-software/go-hsdp-signer"
  "net/http"
)

func signFilter(req *http.Request, sharedKey, secretKey string) (*http.Request, error) {
    s, err := signer.New(sharedKey, secretKey)
    if err != nil {
        return nil, err
    }
    s.SignRequest(req)
    return req, nil
}

```
## License

Licensed is MIT
