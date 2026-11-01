# Austria Cadastral Parcels & Grundstück Lookup MCP (Österreich)

[Deutsch](#deutsch)

Connect your AI assistant (Claude, ChatGPT, Cursor) to [BumiAtlas](https://bumiatlas.com) for Austrian land research through the Model Context Protocol (MCP).

This listing is a focused entry point for:

- Austrian cadastral parcels from BEV's Kataster (Digitale Katastralmappe and Grundstücksverzeichnis, as of 1 April 2026)
- Parcel lookup by Katastralgemeinde and Grundstücksnummer (`30001-2585/1`, `KG 30001 GST 2585/1`), a whole KG (paged), or coordinates
- Each parcel's land uses from the Grundstücksverzeichnis: Benützungsart and Nutzung codes, area per use, yield rating (Ertragsmesszahl) and land-register entry (Einlagezahl)
- Satellite and street map images of a parcel and its neighbours, labelled by Grundstücksnummer

Parcels have no owner information: an Einlagezahl is a land-register entry number, not a person.

## Connect

```
https://bumiatlas.com/mcp/austria
```

Add it as a custom connector in any MCP client and sign in with Google. Tools, examples and data notes: [bumiatlas.com/mcp-docs/austria](https://bumiatlas.com/mcp-docs/austria).

- **Claude:** Settings → Connectors → Add custom connector, paste the URL, then Connect.
- **ChatGPT:** Settings → Apps & Connectors → Advanced → Developer mode, then Create with the URL and OAuth authentication.

## Tools

| Tool | Description |
|---|---|
| `AT_parcel_search` | Find parcels by KG and Grundstücksnummer, a whole KG (paged), or `latitude, longitude`; each result is the whole record with its land uses, the boundary as GeoJSON on request |
| `AT_parcel_image` | Satellite or street map image of a parcel or point, with every parcel in view outlined and labelled with its Grundstücksnummer |

## Example prompts

- *"Which parcel is at 48.2082, 16.3738? What is it used for?"*
- *"Look up KG 30001 GST 2585/1 and show it on satellite imagery."*
- *"List the parcels of Katastralgemeinde 30001."*
- *"How much of this parcel is farmland, and what is its yield rating?"*

## Data source

Parcels © BEV – Bundesamt für Eich- und Vermessungswesen, Kataster (CC BY 4.0).

## Deutsch

Verbinden Sie Ihren KI-Assistenten (Claude, ChatGPT oder Cursor) über das Model Context Protocol (MCP) mit [BumiAtlas](https://bumiatlas.com), um österreichische Grundstücke zu recherchieren.

- Grundstücke aus dem Kataster des BEV, mit den Nutzungen aus dem Grundstücksverzeichnis
- Suche nach Katastralgemeinde und Grundstücksnummer (`30001-2585/1`) oder nach Koordinaten
- Satelliten- und Straßenkarten eines Grundstücks und seiner Nachbarn

Keine Eigentümerdaten: Die Einlagezahl ist eine Grundbuchnummer, keine Person.

**Verbinden:** Fügen Sie `https://bumiatlas.com/mcp/austria` in einem MCP-Client als Custom Connector hinzu und melden Sie sich mit Google an. Die Tool-Namen sind englisch, der Assistent kann aber auf Deutsch antworten.
