This is a quick sketch of how set.mm could be split up.
Statements are separated by newline, new theorems are separated by an additional newline.
Axioms and definitions correspond to $a statements, constants to $c, floatings to $f and variable to $v
Theorems contain only theorem relevant informations $d and $p.

Proof verification is done per proof file, it loads all theorems from the listed imports. Each proof file is done independently.
The verifier needs to make sure that the dependencies have no cycles.

The LSP dynamically loads the imported files (and only the imported files)
The search engine searches the imported files only.
Autocomplete uses the imported files only.

This allows "exotic theorems" to never be loaded.