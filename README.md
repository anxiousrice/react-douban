**豆瓣电影**

1.设置跨域

```js
app.use('*', function (req, res, next) {

	// 设置请求头为允许跨域

    res.header("Access-Control-Allow-Origin", "*");

    // 设置服务器支持的所有头信息字段

    res.header("Access-Control-Allow-Headers", "Content-Type,Content-Length, Authorization, Accept,X-Requested-With");

    // 设置服务器支持的所有跨域请求的方法

    res.header("Access-Control-Allow-Methods", "POST,GET");

    next();

});
```

2. Ant按需导入

   1. 导入插件运行 cnpm i babel-plugin-import --save-dev

   2. 修改.babelrc文件

   3. ```
       ["import", { "libraryName": "antd", "style": "css" }]
      ```

3. 使用react-router-dom实现路由跳转

4. fetch api调用接口

   ```
    componentWillMount() {
       fetchJSONP('https://api.douban.com/v2/movie/subject/' + 						this.props.match.params.id)
         .then(res => res.json())
         .then(data => {
           this.setState({
             info: data,
             isloading: false
           })
         })
     }
   ```

   5.渲染列表

   

   