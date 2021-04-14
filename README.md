# 163 Marker ![](https://img.shields.io/badge/python-3-blue?style=flat-square)

为歌曲添加 `163 key(Don't modify)` 标记

让非网易云客户端下载的音频文件能被客户端识别，正常匹配歌词和查看评论 (与云盘匹配无关)

## Dependency

```
$ pip install -r requirements.txt
```

## Usage

app.py 主程序打开其中一个函数使用

### Main 命令行传参

```sh
$ python 163marker/app.py -h
usage: 163marker [-h] file [uri] [id]

positional arguments:
  file        audio file path (MP3/FLAC)
  uri         meta data source (URL/PATH)
  id          specific song id

optional arguments:
  -h, --help  show this help message and exit
```

- `file` 文件路径 (支持 MP3 和 FLAC 格式)
- `uri` 用户动态 / 专辑 / 歌曲链接 (客户端内分享，复制链接) 或文件路径 (拷贝标记)
- `id` 强制填充歌曲 ID (可选)

### Worker 直接填写

```
load_dir = ''  # 需要marker的文件夹路径

marker_dict = {
    'file1': 'uri1',  # 文件名，链接
    ...
}
```
