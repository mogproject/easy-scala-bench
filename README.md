# easy-scala-bench
Run sbt-jmh in easy way.

## Dependencies

- sbt
- /bin/sh

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

