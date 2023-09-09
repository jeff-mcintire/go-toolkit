# Web Toolkit in Go

A simple example of how to create a reusable Go module with commonly used tools.

The included tools are:

- [ ] Read JSON
- [ ] Write JSON
- [ ] Produce a JSON encoded error response
- [X] Upload a file of files to a specified directory
- [X] Download a static file
- [X] Get a random string of length n
- [ ] Post JSON to a remote service
- [X] Create a directory, including all parent directories, if it does not already exist
- [X] Create a URL safe slug from a string

## Function Notes
**Name:** Slugify
**Input(s):** String
**Output(s):** String with any special character stripped out and spaces replaced by dashes
**Sample:** ```slug, err := tool.Slugify("string")```

**Name:** CreateDirIfNotExist
**Notes:** accepts a string, parses it and creates a directory and any parent directories if they do not exist.
**Sample:** ```err := tool.CreateDirIfNotExist("./testdata/myDir")```

**Name:** RandomString
**Notes:** accepts an int and returns a random string of int length.
**Sample:** ```s := tool.RandomString(10)```

**Name:** DownloadStaticFile
**Notes:** forces a file to be downloaded and not displayed in a browser.
**Sample:** ```tool.DownloadStaticFile(rr, req, "./testdata/pic.jpg", "puppy.jpg")```

**Name:** UploadFiles
**Notes:** Multi file uploader
**Sample:** ```uploadedFiles, err := testTools.UploadFiles(request, "./testdata/uploads/", e.renameFile)```

**Name:** UploadOneFile
**Notes:** Helper function that will upload one  file
**Sample:** ```uploadedFiles, err := testTools.UploadOneFile(request, "./testdata/uploads/", true)```

## Installation

`go get github.com/jeff-mcintire/go-toolkit/`