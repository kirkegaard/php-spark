# Spark
### Sparklines for your shell

See? Here's a graph of your productivity gains after using spark: ▁▂▃▅▇

![Spark in PHP](https://github.com/ranza/php-spark/raw/master/ssdump.png)

## Usage

Regular usage:  
`$ spark 1,2,3,4,5`

Using stdin:  
`$ echo "1,2,3,4,5" | spark --stdin`

## Cooler usage

There's a lot of stuff you can do.

Number of commits to the github/github Git repository, by author:

```bash
$ git shortlog -s |
      cut -f1 |
      tr "\n" ',' |
      sed 's/ //g' |
      spark
  ▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▃▁▁▁▁▁▁▁▁▂▁▁▅▁▂▁▁▁▂▁▁▁▁▁▁▁▁▂▁▁▁▁▁▁▁▁▁▁▁▁▁▁
```

Magnitude of earthquakes over 1.0 in the last 24 hours:

```bash
$ curl http://earthquake.usgs.gov/earthquakes/catalogs/eqs1day-M1.txt --silent | 
  sed '1d' |
  cut -d, -f9 |
  tr "\n" ',' |
  sed 's/ //g' |
  spark
  ▅▆▂▃▂▂▂▅▂▂▅▇▂▂▂▃▆▆▆▅▃▂▂▂▁▂▂▆▁▃▂▂▂▂▃▂▆▂▂▂▁▂▂▃▂▂▃▂▂▃▂▂▁▂▂▅▂▂▆▆▅▃▆
```

Code visualization. The number of characters of `spark` itself, by line, ignoring empty lines:

```bash
$ awk '{ print length($0) }' spark |
  grep -Ev 0 |
  tr "\n" ',' |
  spark
  ▁▁▁▁▅▁▇▁▁▅▁▁▁▁▁▂▂▁▃▃▁▁▃▁▃▁▂▁▁▂▂▅▂▃▂▃▃▁▆▃▃▃▁▇▁▁▂▂▂▇▅▁▂▂▁▇▁▃▁▇▁▂▁▇▁▁▆▂▁▇▁▂▁▁▂▅▁▂▁▆▇▇▂▁▂▁▁▁▂▂▁▅▁▂▁▁▃▁▃▁▁▁▃▂▂▂▁▁▅▂▁▁▁▁▂▂▁▁▁▂▂
```

## Wicked cool usage

Sounds like a wiki is a great place to collect all of your 
[wicked cool usage](https://github.com/holman/spark/wiki/Wicked-Cool-Usage) for spark.

## ▇▁ ⟦⟧ ▇▁

This is a [@holman][holman] joint.

[dotfiles](https://github.com/holman/dotfiles)  
[bin](https://github.com/holman/spark/blob/master/spark)  
[wiki](https://github.com/holman/spark/wiki/Wicked-Cool-Usage)  
[holman](https://twitter.com/holman)
