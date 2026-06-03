# Cypher

Syntax highlighting for the [Neo4j Cypher](https://neo4j.com/docs/cypher-manual/current/) query language in Sublime Text 3 and 4.

This is a modern, minimal `.sublime-syntax` definition. It replaces the long-unmaintained [Sublime Text 2 plugin](https://github.com/kollhof/sublime-cypher).

## Features

- Highlights clauses (`MATCH`, `MERGE`, `RETURN`, `WITH`, `UNWIND`, `CALL`/`YIELD`, `FOREACH`, `LOAD CSV`, schema commands, etc), word operators (`AND`, `OR`, `STARTS WITH`, `IS NULL`, etc), and `CASE`/`WHEN`/`THEN`/`ELSE`/`END`.
- Built-in functions (`count`, `collect`, `coalesce`, `toInteger`, `point`, `date`, etc) highlighted only when actually called, so a variable named `size` or `type` stays plain.
- Namespaced procedure and function calls (`apoc.*`, `gds.*`, `db.*`) highlighted via a pattern, so no stale hardcoded procedure list to maintain.
- Node labels and relationship types (`:Person`, `:KNOWS`), property access (`n.name`), and parameters (`$param`, `$0`).
- String literals (single, double, and backtick-escaped identifiers) with escape sequences, and numeric literals (integers, floats, scientific notation, hex `0x`, octal `0o`, `Inf`/`NaN`).
- Line (`//`) and block (`/* */`) comments.

Colors come entirely from standard TextMate scope names, so the package works with any color scheme.

## Installation

### Package Control (recommended, once published)

1. Open the command palette (<kbd>Ctrl</kbd>/<kbd>Cmd</kbd>+<kbd>Shift</kbd>+<kbd>P</kbd>).
2. Run **Package Control: Install Package**.
3. Search for **Cypher** and install it.

### Manual

1. Run **Preferences > Browse Packages** in Sublime Text.
2. Copy this repository's files into the `Packages > User` directory.

## Usage

Files with a `.cypher` or `.cyp` extension are detected automatically. For any other file, choose **View > Syntax > Cypher**, or edit the `Cypher.sublime-settings` file to add any other extension you want.

## License

MIT: see [LICENSE](LICENSE).
