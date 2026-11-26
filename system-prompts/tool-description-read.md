# Tool Description: read

- Name: Read
- Source: native-prompt-markdown-tool

## Summary

Reads files from the local filesystem.

# Raw Prompt Text
Reads a file from the local filesystem.

- `file_path` must be an absolute path.
- Reads up to ${NUM} lines by default.
- When you already know which part of the file you need, only read that part. This can be important for larger files.
- Results are returned using cat -n format, with line numbers starting at ${NUM}
- Reads images (PNG, JPG, …) and presents them visually. Reads PDFs via the `pages` parameter (e.g. "${NUM}-${NUM}", max ${NUM} pages${PATH}; required for PDFs over ${NUM} pages). Reads Jupyter notebooks (.ipynb) as cells with outputs.
- Reading a directory, a missing file, or an empty file returns an error or system reminder rather than content.
- Do NOT re-read a file you just edited to verify — Edit${PATH} would have errored if the change failed, and the harness tracks file state for you.
{
  "$schema": "${URL}
  "type": "object",
  "properties": {
    "file_path": {
      "description": "The absolute path to the file to read",
      "type": "string"
    },
    "offset": {
      "description": "The line number to start reading from. Only provide if the file is too large to read at once",
      "type": "integer",
      "minimum": ${NUM},
      "maximum": ${NUM}
    },
    "limit": {
      "description": "The number of lines to read. Only provide if the file is too large to read at once.",
      "type": "integer",
      "exclusiveMinimum": ${NUM},
      "maximum": ${NUM}
    },
    "pages": {
      "description": "Page range for PDF files (e.g., \"${NUM}-${NUM}\", \"${NUM}\", \"${NUM}-${NUM}\"). Only applicable to PDF files. Maximum ${NUM} pages per request.",
      "type": "string"
    },
    "allow_large": {
      "description": "Set to true to read a text file, or a line range of one, that is over the usual size limits, up to what still fits in your context. Only use this when you genuinely need all of it or the user asked for the whole file; otherwise read it in parts with offset and limit, or search it.",
      "type": "boolean"
    }
  },
  "required": [
    "file_path"
  ],
  "additionalProperties": false
}
