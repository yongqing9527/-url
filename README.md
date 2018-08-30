# -url
### js获取url传递参数，js获取url？号后面的参数
  
        <Script language="javascript">  
             function GetRequest() {
                var url = location.search; //获取url中"?"符后的字串
                var theRequest = new Object();
                if (url.indexOf("?") != -1) {
                    var str = url.substr(1);
                    strs = str.split("&");
                    for(var i = 0; i < strs.length; i ++) {
                        theRequest[strs[i].split("=")[0]] = unescape(strs[i].split("=")[1]);
                        //unescape(string) 解码   escape() 对字符串进行编码
                    }
                }
                return theRequest;
            }
        </script> 
        
设置或获取对象指定的文件名或路径。
* window.location.pathname
* 例：http://localhost:8086/topic/index?topicId=361
* alert(window.location.pathname); 则输出：/topic/index

设置或获取整个 URL 为字符串。
* window.location.href
* 例：http://localhost:8086/topic/index?topicId=361
* alert(window.location.href); 则输出：http://localhost:8086/topic/index?topicId=361

设置或获取与 URL 关联的端口号码。
* window.location.port
* 例：http://localhost:8086/topic/index?topicId=361
* alert(window.location.port); 则输出：8086

设置或获取 URL 的协议部分。
* window.location.protocol
* 例：http://localhost:8086/topic/index?topicId=361
* alert(window.location.protocol); 则输出：http:

设置或获取 href 属性中在井号“#”后面的分段。
* window.location.hash

设置或获取 location 或 URL 的 hostname 和 port 号码。
* window.location.host
* 例：http://localhost:8086/topic/index?topicId=361
* alert(window.location.host); 则输出：http:localhost:8086

设置或获取 href 属性中跟在问号后面的部分。
* window.location.search
* 例：http://localhost:8086/topic/index?topicId=361
* alert(window.location.search); 则输出：?topicId=361

#### window.location
属性                  描述
* hash                设置或获取 href 属性中在井号“#”后面的分段。
* host                 设置或获取 location 或 URL 的 hostname 和 port 号码。
* hostname      设置或获取 location 或 URL 的主机名称部分。
* href                  设置或获取整个 URL 为字符串。
* pathname      设置或获取对象指定的文件名或路径。
* port                  设置或获取与 URL 关联的端口号码。
* protocol          设置或获取 URL 的协议部分。
* search            设置或获取 href 属性中跟在问号后面的部分。

      $.ajax({
          url: '',
          type: 'POST',
          contentType: 'application/json; charset=UTF-8',
          data: JSON.stringify({}), //从一个对象中解析出字符串
          dataType: 'json',
          headers: {
              Accept: 'bearer ' + postToken
          },
          success: function(text) {
              console.log(text);
          }
      })
      
      var errorBad = new Object();
      var x = Object.keys(errorBad).reverse(); //返回errorBad 这个对象的键组成的数组 的倒序
      var y = Object.keys(errorBad).map(function (key) {
          return errorBad[key];
      }).reverse();
