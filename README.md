forked from [trytofix](https://github.com/trytofix/hexo_weibo_image)

## 使用方法 ##

新建一个配置文件weibo_conf.json, 配置范本:

``` json
{
    "cookie_file": "cookie.txt",
    "weibo_domain": [1, 2, 3, 4],
    "weibo_account": [
        {"usn": "wrong1", "pwd": "wrong1"},
        {"usn": "wrong2", "pwd": "wrong2"},
        {"usn": "wrong3", "pwd": "wrong3"},
        {"usn": "13114348287", "pwd": "hldh214"}
    ]
}
```
微博账号按所给格式加到weibo_account里, 脚本检测到账号不能登陆会自动切换下一个账号进行后续操作

测试脚本

``` bash
python weibo_util.py -f /path/to/the/image
```

## 图片尺寸 ##

ww4.sinaimg.cn/图片尺寸/804691d1gw1f53vdieys0j205m05m3yb

- thumb150 格式：
将原始图片不论大小，有截取地缩放为宽高均为 150像素 的小型图片（不保持纵横比）。
- mw600 格式：
如果原始图片宽度超过 600像素，则将其缩小为宽度为 600像素 的中型图片（保持纵横比）。
- large 格式：
原始图片规格，不进行处理。
- square 格式：
将原始图片尽可能无截取地缩放为宽高均为 80像素 的超小型图片（保持纵横比）。
- thumbnail 格式：
将原始图片尽可能无截取地缩放为宽高均为 120像素 的小型图片（保持纵横比）。
- bmiddle 格式：
如果原始图片宽高其中一边超过 400像素，则将其最长边缩小为 400像素 的中型图片（保持纵横比）。

[参考资料](http://inn-studio.com/sinapic-ext/)
