# Exclude

Here is the default value for Jekyll 3:

```yaml
exclude:
  - vendor/
  - Gemfile
  - Gemfile.lock
  - node_modules/
```

The vendor folder is actually ignored as `"vendor/bundle/", "vendor/cache/", "vendor/gems/", "vendor/ruby/"`.

When you override `exclude`, you must also include those base values. Note that in Jekyll 4 that is not the case.

Using system and custom values.

```yaml
exclude:
  - docs/
  - vendor/
  - Gemfile
  - Gemfile.lock
  - LICENSE
  - Makefile
  - README.md
  - sample*.png
```

You may use a globstar pattern.

```yaml
exclude:
  - "*.png"
```

However, using `/*.png` doesn't work so images are removed at all levels such as assets.

Therefore rather ignore explicitly:

```yaml
exclude:
  - sample.png
```

Or:

```yaml
exclude:
  - sample*.png
```