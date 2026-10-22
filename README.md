# -MINI-SEARCH-ENGINE-
A mini search engine in Java uses a HashMap as an inverted index (word → set of document IDs) for O(1) lookups, and a TreeMap to keep words sorted for prefix search and autocomplete. Queries are tokenized, matched, and ranked by term frequency.
