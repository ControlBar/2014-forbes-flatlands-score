# Scoring Log

With this repo and [flare-timing](https://github.com/BlockScope/flare-timing)
cloned as siblings the following commands show how to score all tasks at once
for the **Australian National Hang Gliding Championships 2014** competition.

```
> ../bin/extract-input --file=forbes2014.fsdb
Extracted 7 tasks from "Australian National Hang Gliding Championships 2014"
Extracting tasks completed in 1.06 s

> ../bin/task-length --file=forbes2014.comp-input.yaml
forbes2014.comp-input.yaml
Measuring task lengths completed in 3.71 m

> ../bin/cross-zone --file=forbes2014.comp-input.yaml
Reading competition from 'forbes2014.comp-input.yaml'
Tracks crossing zones completed in 33.26 s

> ../bin/tag-zone --file=forbes2014.cross-zone.yaml
Reading zone crossings from 'forbes2014.cross-zone.yaml'
Tagging zones completed in 517.72 ms

> ../bin/align-time --file=forbes2014.comp-input.yaml
Reading competition from 'forbes2014.comp-input.yaml'
Reading flying time range from 'forbes2014.cross-zone.yaml'
Reading zone tags from 'forbes2014.tag-zone.yaml'
Aligning times completed in 19.22 m

> ../bin/discard-further --file=forbes2014.comp-input.yaml
Reading competition from 'forbes2014.comp-input.yaml'
Reading task length from 'forbes2014.task-length.yaml'
Reading zone tags from 'forbes2014.tag-zone.yaml'
Filtering times completed in 26.49 s

> ../bin/mask-track --file=forbes2014.comp-input.yaml
Reading competition from 'forbes2014.comp-input.yaml'
Reading task length from 'forbes2014.task-length.yaml'
Reading flying time range from 'forbes2014.cross-zone.yaml'
Reading zone tags from 'forbes2014.tag-zone.yaml'
Masking tracks completed in 29.23 s

> ../bin/land-out --file=forbes2014.comp-input.yaml
Reading land outs from 'forbes2014.mask-track.yaml'
Land outs counted for distance difficulty completed in 63.96 ms

> ../bin/gap-point --file=forbes2014.comp-input.yaml
Reading pilots absent from task from 'forbes2014.comp-input.yaml'
Reading pilots that did not fly from 'forbes2014.cross-zone.yaml'
Reading start and end zone tagging from 'forbes2014.tag-zone.yaml'
Reading masked tracks from 'forbes2014.mask-track.yaml'
Reading distance difficulty from 'forbes2014.land-out.yaml'
Tallying points completed in 657.72 ms
```
