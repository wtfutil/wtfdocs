---
title: "Football"
date: 2019-10-25T17:20:48-07:00
draft: false
weight: 25
---

Displays Football statistics about the specific league. This widget uses [football-data.org](https://www.football-data.org/client/register).

#### Standings

Standings is the ranking or table for specific league. By default it shows top 5 teams in the league but which can be customized using configuration.

#### Matches Played

Shows recent matches played in the specific league. By default it shows matches played in last 5 days.

#### Upcoming Matches

Shows upcoming matches or fixtuers in the specific league. By default it shows upcoming matches for next 5 days.

## Supported Leagues

Currently this widget only support below mentioned league/competition, You should use below shortname of the league in your configuration:

| Competition                      | Short Name |
|----------------------------------|:----------:|
| Brazil Série A                   |     BSA    |
| Campeonato Brasileiro da Série A |     EL2    |
| English Championship             |     EC     |
| English Premier League           |     PL     |
| European Championship            |     EUC    |
| FIFA World Cup                   |     WC     |
| French Ligue 1                   |     FL1    |
| German Bundesliga                |     GB     |
| Italy Serie A                    |     ISA    |
| Netherlands Eredivisie           |     NE     |
| Portugal Primeira Liga           |     PPL    |
| Spain Primera Division           |     SPD    |
| UEFA Champions League            |     CL     |

## Configuration

{{< code lang="yaml" >}}
football:
  enabled: true
  apiKey: "*************"
  league: "PL"
  favTeam: "Liverpool FC"
  standingCount: 5
  matchesFrom: 5
  matchesTo: 5
  position:
    top: 1
    left: 0
    height: 4
    width: 3
  refreshInterval: 1000
  title: "⚽"
{{< /code >}}

| Name          |                                                                                Description                                                                               | Value                                                                                   |
|---------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|-----------------------------------------------------------------------------------------|
| apiKey        | API key to get the football stats from  football-data.org. You can get your Free tier  key on [football-data.org](https://www.football-data.org/client/register) | Your API key or leave it empty to use the WTF_FOOTBALL_API_KEY environment variable.    |
| league        |                                                                     Short Name of the league or competition (Listed above in [Supported Leagues](#supported-leagues))                                                                    | Your league name or leave it empty to use the WTF_FOOTBALL_LEAGUE environment variable. |
| favTeam       | Name of the favorite team from specific league.                                                                                                                          | Your favTeam name or leave it empty to use the WTF_FOOTBALL_TEAM environment variable.  |
| matchesFrom   | List all matches played in last (N) number of days. Default 5                                                                                                            | Any positive integer.                                                                   |
| matchesTo     |                                                  List all upcoming matches coming in next (N) number of days. Default 5                                                  | Any positive integer.                                                                   |
| standingCount | List top number (N) of teams in the league. Default 5                                                                                                                    | Any positive integer.                                                                   |

## Screenshots

<img class="screenshot" src="/imgs/modules/football.png" width="720" height="292" alt="football screenshot" />

{{% sourcePath module="football" %}}