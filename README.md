# Knowledge Graph

An accessible relationship graph for communications compliance. It maps employees, external contacts, messaging accounts, phone numbers and trades as one network, so an analyst can spot the backchannel before reading a single message.

The site is a single page, `index.html`. Open it in a browser; no build step.

## Pages

- **Overview:** what the graph is for and what this version does differently.
- **Explorer:** the working graph. Choose resource types and channels, center on any resource, set a node limit (10 by default, up to 30), size nodes by message volume, and group by team or firm. Read the same view as a graph, a table, or a written summary. Selecting a resource rebuilds the graph around it. Select a relationship or signal to see details, channel volumes, and cross-channel threads. Lines carry an arrowhead at each end, sized by the messages flowing that way.
- **Relationship timeline:** select a line (or press E on a focused node) to open a near-full-screen view: the conversation flow in each direction, daily volume against the pair's mean ± kσ (1, 2 or 3σ), send times against the pair's usual hours, a list of anomalies, and a conversation panel that highlights policy flags (off-channel, information barrier, secrecy language, possible inside information, possible collusion).
- **Data model:** node and edge types, edge properties, and example Cypher and GraphQL (Relay-style, paged at 50).
- **Accessibility:** keyboard map, the three reading layers, and the rules the graph follows.

## Design rules

- Same look as Accessible Charts and Enterprise Library: Geist and Geist Mono, ink on paper, patterns in place of color. Navigation runs horizontally across the header.
- Resource types differ by shape and fill. Captured channels are solid lines, uncaptured are dashed, ownership and trade links are dotted. Signals add a dashed ring and a diamond on the line.
- Color appears only in warnings, always with an icon and words.
- 10 nodes by default, never more than 30. When more match, they're ranked by signals and connection strength, and the page says how many are hidden.
- Light, dark, Windows High Contrast; reduced motion respected. Targets WCAG 2.2 AA.

## Sample data

Coruscant Capital, a fictional investment bank staffed by Star Wars characters, over a 30-day window. Every message and number is invented. The data includes a few scripted stories (Lando and Jyn crossing the information barrier ahead of a Kuat Drive Yards downgrade, Qi’ra and the Hutt Cartel on WeChat, Hondo and Shu Mai before a rates fix, Han and a HoloNet reporter on WhatsApp, an unattributed WhatsApp number) so each signal type has something to show.

## Status

v0.1 preview.
