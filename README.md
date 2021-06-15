# fastdownload

```python
d = FastDownload(dir='~/.fastai', archive='archive', dest='data')
d.download(url) # download to .fastai/archive unless exists; untar to .fastai/data unless exists
```

If archive/dest not provided, try to find them in config file in `dir` if available.

```
{
  'ADULT': [
    "http://files.fast.ai/data/examples/adult_sample.tgz",
    968212,
    "64eb9d7e23732de0b138f7372d15492f"
  ]
}
```

```
{
  'ADULT': "http://files.fast.ai/data/examples/adult_sample.tgz"
}
```
