# Web Toolkit for Go

A simple example of how to create a reusable Go module with commonly used tools.

The included tools are:

- [X] Read JSON
- [X] Write JSON
- [X] Produce a JSON encoded error response
- [X] Upload a file of files to a specified directory
- [X] Download a static file
- [X] Get a random string of length n
- [X] Post JSON to a remote service
- [X] Create a directory, including all parent directories, if it does not already exist
- [X] Create a URL safe slug from a string

## Function Notes
**Name:** Slugify <br />
**Input(s):** String <br />
**Output(s):** String with any special character stripped out and spaces replaced by dashes <br />
**Sample:** ```slug, err := tool.Slugify("string")``` <br />
<br />
**Name:** CreateDirIfNotExist <br />
**Notes:** accepts a string, parses it and creates a directory and any parent directories if they do not exist. <br />
**Sample:** ```err := tool.CreateDirIfNotExist("./testdata/myDir")``` <br />
<br />
**Name:** RandomString <br />
**Notes:** accepts an int and returns a random string of int length. <br />
**Sample:** ```s := tool.RandomString(10)``` <br />
<br />
**Name:** DownloadStaticFile <br />
**Notes:** forces a file to be downloaded and not displayed in a browser. <br />
**Sample:** ```tool.DownloadStaticFile(rr, req, "./testdata/pic.jpg", "puppy.jpg")``` <br />
<br />
**Name:** UploadFiles <br />
**Notes:** Multi file uploader <br />
**Sample:** ```uploadedFiles, err := testTools.UploadFiles(request, "./testdata/uploads/", e.renameFile)``` <br />
<br />
**Name:** UploadOneFile <br />
**Notes:** Helper function that will upload one  file <br />
**Sample:** ```uploadedFiles, err := testTools.UploadOneFile(request, "./testdata/uploads/", true)``` <br />
<br />
**Name:** ReadJSON <br />
**Notes:** tries to read the body of a request and converts from json into a go data variable <br />
**Sample:** ```err = testTool.ReadJSON(rr, req, &decodedJSON)``` <br />
<br />
**Name:** WriteJSON <br /> 
**Notes:** takes a response status code and arbitrary data and writes json to the client <br />
**Sample:** ```err := testTools.WriteJSON(rr, http.StatusOK, payload, headers)``` <br />
<br />
**Name:** ErrorJSON <br />
**Notes:** takes an error, & optionally a status code, and generates and sends a JSON error message <br />
**Sample:** ```err := testTools.ErrorJSON(rr, errors.New("some error"), http.StatusServiceUnavailable)``` <br />
<br />
**Name:** PushJSONToRemote <br />
**Notes:** posts arbitrary data to some URL as JSON, and returns the response, status code, and error, if any. <br />
**Sample:** ```_, _, err := testTools.PushJSONToRemote("http://example.com/some/path", foo, client)``` <br />
<br />
## Installation

`go get github.com/jeff-mcintire/go-toolkit/`
