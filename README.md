首先在开发者工具右上角点击 "详情" 在“本地工具" 一栏中选中“不校验合法域名，web-view（业务域名），TLS版本以及https协议”
否则运行测试过程中 wx：request 会检测域名并拦截请求

项目目录
/
|---components
|     |-----MyTitle（公共头部组件）
|
|---icons （矢量图）
|
|---pages
|     |----index (首页)
|     |
|     |---detail (视频详情页)
|
|---styles
|     |---fontawesome.wxss (网络图标矢量图库)



原视频教程黑马程序员：https://www.bilibili.com/video/BV1Ct411p7bj?p=20
  原视频教程提供的接口（经常服务不可用）：
  公共路径：https://easy-mock.com/mock/5c1dfd98e8bfa547414a5278/bili
            接口名词        接口路径            备注
            首页导航        /navList
            首页轮播图      /swiperList
            视频列表        /videosList
            视频详情        /videoDetail?id     需带上视频id
            推荐视频        /othersList?id      需带上视频id
            评论列表        /commentsList?id    需带上视频id


备用接口:
  首页导航：http://mock-api.com/mnEe4VnJ.mock/navList
  轮播图：http://mock-api.com/mnEe4VnJ.mock/swiperList
  视频列表：http://mock-api.com/mnEe4VnJ.mock/videoList
  视频详情：http://mock-api.com/mnEe4VnJ.mock/videoDetail
  推荐视频：http://mock-api.com/mnEe4VnJ.mock/otherList
  评论列表：http://mock-api.com/mnEe4VnJ.mock/commentList


视频接口调用位于 pages/detail/detail.js
原接口,视频详情页，视频一般获取不到视频，但id有效，作者、播放量可正确获取
备用接口有缺陷，视频详情接口id无效，不论点击哪个视频，视频详情显示均为第一个视频信息

可参考其他github项目
https://github.com/yqxshiki/Wechat-applet-imitates-Bili

