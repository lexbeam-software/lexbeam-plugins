# Lexbeam plugins

Plugins for Claude by [Lexbeam Software](https://lexbeam.com): each one adds a German skill and the connection to a
hosted MCP server that answers from typed, sourced data. Each folder is one plugin.

| Plugin | For | Hosted MCP server |
|---|---|---|
| [Installflow](installflow/) | Electricians and planners in North Rhine-Westphalia: what the distribution grid operators require for a wallbox, PV system, heat pump, battery storage or house connection (all 113 listed, rules for 102) | https://mcp.installflow.de/mcp |
| [azubiklar](azubiklar/) | Apprenticeship seekers and their advisers around Münster: Ausbildung listings typed for access attributes such as "Hauptschulabschluss reicht" | https://mcp.azubiklar.de/mcp |
| [Normlotse](normlotse/) | External data protection, information security and AI officers: new publications of German and EU regulators and courts, matched to client profiles, with a monthly proof of monitoring | https://mcp.normlotse.de/mcp |

The servers need no login. Their basic tools are free; the tools marked Pro take a licence key that the user
states in the conversation. Answers are in German.

## Install in Claude Code

```bash
claude plugin marketplace add lexbeam-software/lexbeam-plugins
claude plugin install installflow@lexbeam-plugins
```

Replace `installflow` with `azubiklar` or `normlotse` for the other plugins.

## Data and privacy

Every plugin's README has a section "Daten und Datenschutz" that names what the plugin sends and where. In
short: the plugins ship Markdown skills and one MCP connection each, run no hooks or scripts, and send tool
arguments only to their own server, hosted by Scaleway in Paris. The servers store no tool arguments or results
and set no cookies; each server's privacy policy is linked from its README.

## License

The files in this repository are licensed under Apache-2.0 (see LICENSE). The hosted servers and their data are
services of Lexbeam Software, Speditionstraße 15A, 40221 Düsseldorf, Germany
([imprint](https://www.lexbeam.com/de/impressum)).
