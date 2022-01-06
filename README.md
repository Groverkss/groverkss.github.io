## Developing

Serve using jekyll:

```bash
bundle exec jekyll serve -w
```  

## Publish

First, change baseurl in `_config.yml` to `groverkss.github.io`.

Publish using rake: 

```bash
rake publish
```

Change back the baseurl in `_config.yml` to empty.
