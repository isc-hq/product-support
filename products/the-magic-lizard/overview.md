# What Is The Magic Lizard?

The Magic Lizard is a single-binary, zero-dependency multi-industry (including healthcare) integration middleware. Think of it as a modern, developer-friendly replacement for legacy ESB platforms like Interfaceware Iguana, Mirth Connect or Rhapsody ... but without the JVM bloat, without the drag-and-drop complexity, and with a code-first TypeScript transformation engine. It is designed to be extremely lightweight with a small footprint to achieve maximum performance output for use in transaction environments.

At a high level, it moves data between systems through **pipelines**. Each pipeline has three stages:

1. **Ingestor** — receives data (HTTP webhook, SFTP poll, MLLP/HL7 TCP, database poll)
2. **Transformer** — TypeScript code that reshapes the data (runs in an isolated Deno sandbox)
3. **Dispatcher** — sends transformed data to its destination (HTTP, SFTP, MLLP, database, filesystem)

Everything ships as a single native executable (~30–50 MB) with an embedded SQLite database. No Node.js, no Nginx, no external database required.
