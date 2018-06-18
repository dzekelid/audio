---
swagger: "2.0"
x-collection-name: GoToMeeting
x-complete: 1
info:
  title: Go To Webinar
  description: the-gotowebinar-api-provides-seamless-integration-of-webinar-registrant-and-attendee-data-into-your-existing-infrastructure-or-thirdparty-applications--the-ability-to-register-participants-as-well-as-pull-lists-of-registrants-and-attendees-for-a-webinar-allows-organizers-to-manage-the-flow-of-information-between-their-primary-applications-without-manual-intervention-
  termsOfService: https://developer.citrixonline.com/terms-use
  contact:
    name: Developer Support
    url: https://developer.citrixonline.com
    email: developer-support@citrixonline.com
  version: 1.0.0
host: api.citrixonline.com
basePath: /G2W/rest
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /organizers/{organizerKey}/webinars/{webinarKey}/audio:
    get:
      summary: Get audio information
      description: Retrieves the audio/conferencing information for a specific webinar.
      operationId: getAudioInformation
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeyaudio-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Webinars
      - WebinarKey
      - Audio
    post:
      summary: Update audio information
      description: Updates the audio/conferencing settings for a specific webinar
      operationId: updateAudioInformation
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeyaudio-post
      parameters:
      - in: body
        name: body
        description: The audio/conferencing settings
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      - in: query
        name: notifyParticipants
        description: Defines whether to send notifications to participants
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Webinars
      - WebinarKey
      - Audio
---