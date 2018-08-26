---
swagger: "2.0"
x-collection-name: NewsWhip
x-complete: 0
info:
  title: News Whip API Publisher
  description: Search news by publisiher.
  termsOfService: http://www.newswhip.com/PrivacyAndLegal
  version: v1
host: api.newswhip.com
basePath: v1/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  publisher/:
    get:
      summary: Publisher
      description: Pull publishers.
      operationId: getPublisher
      x-api-path-slug: publisher-get
      parameters:
      - in: query
        name: key
        description: API Key
      responses:
        200:
          description: OK
      tags:
      - News
      - Publisher
  publisher/{publisher}/{time_period}:
    get:
      summary: Publisher
      description: Search news by publisiher.
      operationId: getPublisherPublisherTimePeriod
      x-api-path-slug: publisherpublishertime-period-get
      parameters:
      - in: query
        name: key
        description: API Key
      - in: path
        name: publisher
        description: Returns all articles published within that domain or subdomain
      - in: query
        name: sort_by
        description: 'One of the following: [default, fb_likes, fb_shares, fb_comments,
          fb_total, twitter, linkedin, fb_tw_and_li, nw_score, nw_max_score]'
      - in: path
        name: time_period
        description: Filters articles published within the last X hours
      - in: query
        name: video_only
        description: true or false
      responses:
        200:
          description: OK
      tags:
      - News
      - Publisher
      - Publisher
      - Time
      - Period
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