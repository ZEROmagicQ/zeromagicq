name: Waka Readme

on:
  # for manual workflow trigger
  workflow_dispatch:
  schedule:
    # runs at 12 AM UTC (5:30 AM IST)
    - cron: "0 0 * * *"

jobs:
  update-readme:
    name: WakaReadme DevMetrics
    runs-on: ubuntu-latest
    steps:
      - uses: athul/waka-readme@master # do NOT replace with anything else
        with:
          GH_TOKEN: ${{ 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 }}
          WAKATIME_API_KEY: ${{ waka_5c0ad78a-4eac-46ae-aa32-6c633710fbc9 }}
          API_BASE_URL: https://wakatime.com/api
          REPOSITORY: YOUR_GITHUB_USERNAME/YOUR_REPOSITORY_NAME
          SHOW_TITLE: true
          SECTION_NAME: waka
          BLOCKS: ->
          CODE_LANG: rust
          TIME_RANGE: all_time
          LANG_COUNT: 10
          SHOW_TIME: true
          SHOW_TOTAL: true
          SHOW_MASKED_TIME: false
