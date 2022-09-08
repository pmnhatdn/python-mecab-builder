# python-mecab-builder

`Python 3.7` with `mecab` builder dependencies.

## How to use
In your `DOCKERFILE` specify your image with a release build as its tag.

e.g. To use this image with the `release-1.1` build you would include something like below:
```yml
    docker:
      - image: bebit/python-mecab-builder:release-1.1
```

## Updating image dependencies

E.g. If you wanted to change from `python 3.7.9` to `python 3.5.6` you would just update the image tag like below:

```diff
- FROM python:3.7-slim-stretch
+ FROM python:3.5-slim-stretch
```

## Releasing
- To release a new docker image, publish a new tag which will trigger Github Action to build and push a new docker image to `ghcr.io/bebit/python-mecab-builder:<tag>`
