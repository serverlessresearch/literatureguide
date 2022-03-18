# Serverless Literature Guide

This *Serverless Literature Guide* aims to provide an overview of a once-niche field that has grown rapidly.

This is the source code for the [web site](https://serverlessresearch.github.io/literatureguide/).

## Contribution Guidelines

A project of this nature is out-of-date immediately so we welcome contributions to help keep it updated.
Work peer reviewed publications (e.g., ACM or IEEE), as well as preprints that have attracted substantial attention make welcome additions.

## Testing Locally

We have found it easiest to use the [Jekyll Docker Image](https://hub.docker.com/r/jekyll/jekyll/) during development.

You may use the command:

```
docker run --rm \
  --volume="$PWD:/srv/jekyll" \
  --publish 4000:4000 \
  jekyll/jekyll \
  jekyll serve
```

Then open a browser at `http://localhost:4000/literatureguide/`.

## Additional notes Notes

* We use the [Jekyll Scholar](https://github.com/inukshuk/jekyll-scholar) plugin.
* Since Jekyll Scholar is not supported natively by GitHub pages, we use a GitHub action to deploy it. See the [Jekyll documentation on GitHub Actions](https://jekyllrb.com/docs/continuous-integration/github-actions/).
* We have formatted the [.bib file](_bibliography/references.bib) using [biblib](https://github.com/aclements/biblib) by Austin Clements.
