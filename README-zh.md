### 中文 | [English](README.md)

# 土拨鼠IPTV，支持udpxy

## [官网](http://www.turboshow.cn)

![输入图片说明](https://images.gitee.com/uploads/images/2019/0727/201458_7b480937_82552.png "screenshot_tv.png")
## IPTV设置
### web界面
`http://{app所在设备IP}:1213`

### Web API
#### 导入播放列表
注：请自行抓包制作播放列表，或者网上找

`POST http://{app所在设备IP}:1213/api/settings/playlist`

body
```
[
    {
        "title": "Channel 1",
        "url": "rtp://239.0.0.1:1234"
    },
    {
        "title": "Channel 2",
        "url": "rpt://239.0.0.2:1234"
    },
    ...
]
```

#### udpxy
如路由器支持udpxy，可设置相应地址进行加速.

`POST http://{app所在设备IP}:1213/api/settings/udpxy`

body
```
{
    "addr": "192.168.1.254:1234"
}
```
关闭udpxy
 
 POST
```
{
    "addr": null
}
```

