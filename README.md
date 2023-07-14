E-mail: mattyhuan7@gmail.com / jh730@duke.edu 

[![GitHub Streak](https://streak-stats.demolab.com?user=Matty-7&theme=dark&hide_border=true&exclude_days=Sat%2CSun)](https://git.io/streak-stats)

name: Waka Readme

on:
  schedule:
    # Runs at 12am IST
    - cron: '30 18 * * *'
  workflow_dispatch:
jobs:
  update-readme:
    name: Update Readme with Metrics
    runs-on: ubuntu-latest
    steps:
      - uses: anmol098/waka-readme-stats@master
        with:
          WAKATIME_API_KEY: ${{ secrets.WAKATIME_API_KEY }}
          GH_TOKEN: ${{ secrets.GH_TOKEN }}
