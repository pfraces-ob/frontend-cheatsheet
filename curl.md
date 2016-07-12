cURL
====

Download file
-------------

    curl -fLo <path/to/dest> --create-dirs <url>

  * `-f`: fail silently on server errors
  * `-L`: follow `3xx` redirections
  * `-o <path/to/dest>`: save output in specified file instead of stdout
  * `--create-dirs`: when used with `-o` will create the necessary local
    directory hierrarchy

POST with JSON payload
----------------------

    curl <url> \
      -X POST \
      -H 'Content-Type: application/json' \
      -d <JSON payload>

  * `-X`: HTTP method (`GET` by default)
  * `-H`: HTTP headers
  * `-d <data>`: payload

`<JSON payload>` can be specified as:

  * JSON string literal
  * `@path/to/file`
  * `-` (stdin)
