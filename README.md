# easy-scala-bench
Run [sbt-jmh](https://github.com/ktoso/sbt-jmh) in easy way.

## Dependencies

- sbt
- Bash (/bin/bash)

## Quickstart

Clone this repository, then move into it.

```
git clone https://github.com/mogproject/easy-scala-bench.git
cd easy-scala-bench
```

Write scala script to benchmark and pipe to ```easy-scala-bench```

```
echo 'for (i <- 1 to 1000) for (j <- 1 to 1000) i + j' | ./easy-scala-bench
```

Enjoy!

## Testing with State

Want to keep state or parameters during tests?  
Write two blocks separated by the line ```====```. The first block will be used for the context and the last one is for the benchmark code.

e.g.

```
echo '
val xs = (1 to 1000000).toList
====
xs.length
' | ./easy-scala-bench
```

In this case, only ```xs.length``` should be measured in the benchmark.