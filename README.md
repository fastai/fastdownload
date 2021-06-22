# FastDownload
> Downloads dataset from `url`. 


A general purpose data download library.

## Install

`pip install fastdownload`

## How to use

`FastDownload` allows you to pass in paths for `archive_path` and `data_path`. Unless specified:
- `archive_path` defaults to `~/.fastai/archive`
- `data_path` defaults to `~/.fastai/data`

`FastDownload` will download the file from `url` to `archive_path` and then un-compress it to `data_path`.

```python
# passing in paths
d = FastDownload(archive_path='./archive', data_path='./data')
d.download(URLs.ADULT_SAMPLE)
```




    Path('data/adult_sample')



Below example shows where data get's downloaded when using default paths.

```python
# using default paths
d = FastDownload()
d.download(URLs.ADULT_SAMPLE)
```




    Path('/home/arora/.fastai/data/adult_sample')



We could also just pass in the URL. This will download `mnist_tiny.tgz` at `archive_path` and untar it at `data_path`. 

```python
# passing in URL which is not part of `URLs` and using default paths
d = FastDownload()
d.download('https://s3.amazonaws.com/fast-ai-sample/mnist_tiny.tgz')
```




    Path('/home/arora/.fastai/data/mnist_tiny')


