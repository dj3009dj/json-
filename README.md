# json-
json作为一种通用的数据格式，在终端与服务端之间的交互中非常常见。<br/>
json本身就是一种跨平台的数据格式，举例而言<br/>
<pre>
JSONObject obj=
"employee":[{
"id":21330043,
"name":
{"nickname":"ajun",
"workname":"sijunding"},
"like":"coding"
}];
</pre>
JSON对象使用{}括号，JSON数组使用[]括号，注意JSON就是一种键值对，其中属性名称(键)只有string这种格式，而属性值有string,integer等格式</br>
<pre>
String str;
JSONObject obj=new JSONObject(str);//使用new可以将字符串转变为JSONObject格式
JSONArray arr=obj.optJSONArray("employee");//可以获得JSON的数组
JSONObject o=arr.getJSONObject(0);//可以获得JSONObject
int id=Integer.parseInt(o.optString("id").toString());//optString表示获取string格式的属性名对应的属性值
</pre>
