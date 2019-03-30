# GLUE dataset download script （fixed）

## 解决方法

如果没法下载，基本上都是因为GFW，你懂得。但是如果翻了墙还不可以下载，那么可以通过以下两种方法来解决。

1. enable http proxy (在shadowsocks中设置)
2. 添加以下三行代码，根据shadowsocks的http proxy listen port填写，多数为1080，需要根据你的个人情况来修改

```python
proxy = urllib.request.ProxyHandler({'http': '127.0.0.1:1080', 'https': '127.0.0.1:1080'})
# construct a new opener using your proxy settings
opener = urllib.request.build_opener(proxy)
# install the openen on the module-level
urllib.request.install_opener(opener)
```

### Reference

https://github.com/nyu-mll/GLUE-baselines.git



