# Web Toolkit in Go

A simple example of how to create a reusable Go module with commonly used tools.

The included tools are:

- [ ] Read JSON
- [ ] Write JSON
- [ ] Produce a JSON encoded error response
- [ ] Upload a file of files to a specified directory
- [ ] Download a static file
- [ ] Get a random string of length n
- [ ] Post JSON to a remote service
- [X] Create a directory, including all parent directories, if it does not already exist
- [X] Create a URL safe slug from a string

## Function Notes
**Name:** Slugify
**Input(s):** String
**Output(s):** String with any special character stripped out and spaces replaced by dashes

**Name:** CreateDirIfNotExist
**Input(s):** String A path
**Output(s):** None



## Installation

`go get github.com/jeff-mcintire/go-toolkit/`