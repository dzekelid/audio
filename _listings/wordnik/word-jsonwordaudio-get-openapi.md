---
swagger: "2.0"
x-collection-name: Wordnik
x-complete: 0
info:
  title: Wordnik Fetches audio metadata for a word.
  description: The metadata includes a time-expiring fileUrl which allows reading
    the audio file directly from the API.  Currently only audio pronunciations from
    the American Heritage Dictionary in mp3 format are supported.
  version: "4.0"
host: api.wordnik.com
basePath: /v4
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /word.json/{word}/audio:
    get:
      summary: Fetches audio metadata for a word.
      description: The metadata includes a time-expiring fileUrl which allows reading
        the audio file directly from the API.  Currently only audio pronunciations
        from the American Heritage Dictionary in mp3 format are supported.
      operationId: getAudio
      x-api-path-slug: word-jsonwordaudio-get
      parameters:
      - in: query
        name: limit
        description: Maximum number of results to return
      - in: query
        name: useCanonical
        description: Use the canonical form of the word
      - in: path
        name: word
        description: Word to get audio for
      responses:
        200:
          description: OK
      tags:
      - Words
      - Audio
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---