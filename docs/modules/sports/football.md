# Football

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

```yaml
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
  refreshInterval: 1000s
  title: "⚽"
```

## Screenshots

<img class="screenshot" src="/assets/modules/football.png" width="720" height="292" alt="football screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="apiKey", desc="API key to get the football stats from  football-data.org. You can get your Free tier  key on <a href='https://www.football-data.org/client/register'>football-data.org</a>. Leave it empty to use the <code>WTF_FOOTBALL_API_KEY</code> environment variable.", value="" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

{% with name="league", desc="Short name of the league or competition (as listed above in <a href='#supported-leagues'>Supported Leagues</a>).", value="" %}
{% include "attributes/custom.md" %}
{% endwith %}

{% with name="favTeam", desc="<em>Optional</em> Name of the favorite team from specific league. Leave it empty to use the <code>WTF_FOOTBALL_TEAM</code> environment variable.", value="" %}
{% include "attributes/custom.md" %}
{% endwith %}

{% with name="matchesFrom", desc="<em>Optional</em> List all matches played in last (N) number of days. Default <code>5</code>.", value="Any positive integer." %}
{% include "attributes/custom.md" %}
{% endwith %}

{% with name="matchesTo", desc="<em>Optional</em> List all upcoming matches coming in next (N) number of days. Default <code>5
</code>.", value="Any positive integer." %}
{% include "attributes/custom.md" %}
{% endwith %}

{% with name="standingCount", desc="<em>Optional</em> List top number (N) of teams in the league. Default <code>5</code>.", value="Any positive integer." %}
{% include "attributes/custom.md" %}
{% endwith %}
    </tbody>
</table>

{% set src="football" %}
{% include "src_path.md" %}