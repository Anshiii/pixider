
# pixider 
爬取pixiv.net的图片并保存。  
默认的任务是爬取个人关注画师昵称和id列表，并以json格式保存  


## 使用
不好意思...暂时只写了个半自动的  
需要先自行登录，将主页响应的cookie写在`config/config.js`的配置里。  

## 运行

```
npm run app.js
```
>node 7.6+


## Api
 * getImagesByUserId(id,option)  
 获取某个用户id的投稿作品
 * getFollowingIllusts(id,option)
 
 * getImageFromRank(option) //未完成  
 获取插画排行榜上的投稿作品，默认为当时的排行榜。
 * getImageByKeyWord(key，option) //未完成  
 获取搜索关键词返回的作品，默认只返回前50项。
 * getFollowingIdList([id])  
 获取指定id用户关注列表，包括id和昵称，默认id参数为cookie所有者，保存为followingIdList.json
 * Option<pre>
  {
  rate:Number,		     //返回大于该分数的图片
  time:String/Array, 	//格式如'20170707'如果参数为字符串，则默认为该从日期至今的作品，如果为数组，则为数组内两个日期之间的作品
  day:String,		   //仅获取该日期的数据
  type:['illust','manga','ugoira']      //限定爬取的图片类型，插画，漫画，动图。默认为插画。
  }
</pre>
