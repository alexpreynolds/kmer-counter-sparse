# kmer-counter-sparse

The `kfs` program reads in multiline FASTA records, counts canonical kmers using Google's [`sparse_hash_map` hash table](https://github.com/sparsehash/sparsehash), and measures time taken to read in and process records.

## Usage

To install `sparse_hash_map` libraries on OS X, use Homebrew: `brew install google-sparsehash`.

### Compilation

```
$ make kfs
```

### Performance

Specify variables `K` (integer) and `FASTA` (path to FASTA sequences).

```
$ /usr/bin/time -l ./kfs -k ${K} -i ${FASTA}
...
```
