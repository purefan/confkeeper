# Configuration Keeper
Takes a list of files and puts them in One private gist. If the target gist already exists it will update it. Gists have versions (named "revisions") so even when a gist is updated you can see a previous version of it.

## Features
- Read a list of file paths and store in a local temporary file
    - use json? think of line breaks
- Authenticate with github
    - Gist api uses oauth, try to read credentials from a file outside this project (~/.github maybe?)
- Upload the local temp file to a private gist
    - Read the name from a configuration setting in package.json
    - Check if the target gist exists
- Download the target gist
    - Extract the gist preserving file paths