---
datapackage:
  name: finance-vix
  profile: data-package
  licenses:
  - id: odc-pddl
    name: open_data_commons_public_domain_dedication_and_license_v1.0
    path: http://opendatacommons.org/licenses/pddl/
    title: Open Data Commons Public Domain Dedication and License v1.0
  resources:
  - dpp:streaming: true
    encoding: utf-8
    format: csv
    mediatype: text/csv
    name: vix-daily
    path: data/vix-daily.csv
    profile: tabular-data-resource
    schema:
      fields:
      - format: any
        name: Date
        type: date
      - format: default
        name: VIX Open
        type: number
      - format: default
        name: VIX High
        type: number
      - format: default
        name: VIX Low
        type: number
      - format: default
        name: VIX Close
        type: number
      missingValues:
      - ''
    title: VIX Daily
  sources:
  - name: CBOE VIX Page
    path: http://www.cboe.com/micro/vix/historical.aspx
    title: CBOE VIX Page
  views:
  - name: graph
    spec:
      group: Date
      series:
      - VIX Close
      type: line
      resources:
      - vix-daily
    specType: simple
    title: VIX - CBOE Volatility Index
---

[Here is the source file on GitHub](https://github.com/datopian/datarich-demo/blob/main/posts/story2.md) used to render this page.

## Some extra content

Here is some extra content written in the body of this markdown file.

<FrictionlessView viewId={0} />
