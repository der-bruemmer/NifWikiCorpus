# Wikipedia NIF corpus creator

Reads triples containing HTML literals as objects, turning them into NIF 2.0 files.

## WikiCorpusGenerator

Expects an NTRIPLES file with HTML Literals containing Wikipedia abstracts. Parses them, cleans the text and produces one nif:Context resource for each abstract and one nif:Word resource for each link. Prints as a number of turtle files because file sizes get unwieldy otherwise. 

## NIFCorpusSurfaceFormEnricher

Takes the generated NIF corpus and a number of surface forms extracted from the corpus with another tool (not contained in this repository). Adds nif:Words for surface forms of entities that were linked in the text to the corpus and writes a new, enriched corpus.

Both classes are in an extremely brittle state. Sorry about that.