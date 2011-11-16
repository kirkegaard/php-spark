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

## Todo / Good to know

 * php-spark doesnt support whitespaces like `1, 2, 3`
 * If you use space as a separator you should quotes like `$ spark "1 2 3 4"`
 * Add support for width by using `-w` as an argument

## ▇▁ ⟦⟧ ▇▁