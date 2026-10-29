# Knowledge Graph

An accessible relationship graph for communications compliance. It maps employees, external contacts, messaging accounts, phone numbers and trades as one network, so an analyst can spot the backchannel before reading a single message.

The site is a single page, `index.html`. Open it in a browser; no build step.

## Pages

- **Overview:** what the graph is for and what this version does differently.
- **Explorer:** the working graph. Choose resource types and channels, center on any resource, set a node limit (50 max), and group by team or firm. Read the same view as a graph, a table, or a written summary. Select a resource, relationship or signal to see details, channel volumes, and cross-channel threads.
- **Data model:** node and edge types, edge properties, and example Cypher and GraphQL (Relay-style, paged at 50).
- **Accessibility:** keyboard map, the three reading layers, and the rules the graph follows.

## Design rules

- Same look as Accessible Charts and Enterprise Library: Geist and Geist Mono, ink on paper, patterns in place of color. Navigation runs horizontally across the header.
- Resource types differ by shape and fill. Captured channels are solid lines, uncaptured are dashed, ownership and trade links are dotted. Signals add a dashed ring and a diamond on the line.
- Color appears only in warnings, always with an icon and words.
- Never more than 50 nodes. When more match, they're ranked by signals and connection strength, and the page says how many are hidden.
- Light, dark, Windows High Contrast; reduced motion respected. Targets WCAG 2.2 AA.

## Sample data

Calder & Wren, a fictional investment bank, over a 30-day window. Every name, number and message is invented. The data includes a few scripted stories (contact across an information barrier ahead of a research downgrade, a WeChat allocation request, a spike before a rates fix, a reporter on WhatsApp, an unattributed WhatsApp number) so each signal type has something to show.

## Status

v0.1 preview.
