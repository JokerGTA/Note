云笔记
=====
### MVC重定向：
` return Redirect("/Demo/Demo/Index"); `

# MVC控制器可返回的类型：
http://www.cnblogs.com/ljl0513/p/4691166.html

# 对象Json化：
(```)
JSON.stringify()
data: { "PutInData": JSON.stringify(listTemp) },
(```)

# 强制浏览器后退刷新页面：
(```)
if (window.name != "bencalie") {
            location.reload();
            window.name = "bencalie";
        } else {
            window.name = "";
        }
(```)        
其他：http://www.jb51.net/article/94239.htm
<a href="http://www.jb51.net/article/94239.html">相关文章</a>

# jq 设置class：
 $("#ZY").attr("class","fl ck_black_color");”

# 弹出层layer:
http://layer.layui.com/
<a href="http://layer.layui.com/">相关文章</a>

# LAMDA查询:
(```)
public List<CarInfoEnt> GetList()
{
    var expression = ExtLinq.True<CarInfoEnt>();
    expression = expression.And(t => t.C_State.Equals(1));
    return service.FindList(expression);
}
(```)

# 可以用前台remove的方法删除，这样就不用拼html了
`$("#"+id).parent().parent().parent().parent().parent().remove();`

# 利用浏览器清除cookies：
(```)
HttpCookie aCookie;
string cookieName;
int limit = Request.Cookies.Count;
for (int i = 0; i < limit; i++)
{
cookieName = Request.Cookies[i].Name;
if (cookieName == "Cookies_CKServiceCheck" || cookieName == "Cookies_CheckPrice")
{
aCookie = new HttpCookie(cookieName);
aCookie.Expires = DateTime.Now.AddDays(-1);
Response.Cookies.Add(aCookie);
}                    
}
(```)

# fileinput文档:
http://plugins.krajee.com/file-basic-usage-demo
<a href="http://plugins.krajee.com/file-basic-usage-demo">相关文章</a>
var imgUpURL = 'http://192.168.1.199:8099/ImgHandler.ashx';
var imgURL = 'http://192.168.1.199:8099';

# js 保留两位小数
http://www.jb51.net/article/45884.htm
<a href="http://www.jb51.net/article/45884.htm">相关文章</a>

// 保留两位小数
num = num.toFixed(2);

// jquery根据name属性查找
$("div[id]") 选择所有含有id属性的div元素 
$("input[name='keleyicom']") 选择所有的name属性等于'keleyicom'的input元素 
$("input[name!='keleyicom']") 选择所有的name属性不等于'keleyicom'的input元素 
$("input[name^='keleyi']") 选择所有的name属性以'keleyi'开头的input元素 
$("input[name$='keleyi']") 选择所有的name属性以'keleyi'结尾的input元素 
$("input[name*='keleyi']") 选择所有的name属性包含'keleyi'的input元素 
$("input[id][name$='keleyi']") 可以使用多个属性进行联合选择，
该选择器是得到所有的含有id属性并且那么属性以keleyi结尾的元素 
例如：$(":input[name='keleyi']") 表示查找的是name为keleyi的表单。
转载自柯乐义：http://keleyi.com/a/bjac/01wjh0a0.htm

// web前端资源：
http://www.cnblogs.com/jihua/p/webfront.html

// 回调路径
D:\StartKitwc\CheKuProject\SourceCode\MZ.Framework\CK.PlatformUI\Configs\system.config

// 设置a标签hover字体颜色
onmouseover="this.style.color = '#f78b25';"

// y隐藏模态框
 $('.modal').modal('hide');

// 利用父级找子集
    $('.editTable').on('click', '.shanchu', function () {
            $(this).parent().parent().remove();
     })
http://localhost:10293/DownLoadHandler.ashx?id=@CKServiceOrder.C_Id&type=KZFW&childtype=KZHT

// 一般处理程序下载
http://blog.csdn.net/qq_18316109/article/details/52383784

// jq 判断点的是第几个元素
console.log($(this).parent().parent().parent().index());

// double&&decimal
http://www.cnblogs.com/lovewife/articles/2466543.html

// 完美限制textarea字数
<textarea id="area" name="ss" placeholder="请输入文本内容"></textarea>  
<p><span id="text-count">20</span>/20</p>  
<script type="text/javascript">  
    /*字数限制*/  
    $("#area").on("input propertychange", function() {  
        var $this = $(this),  
            _val = $this.val(),  
            count = "";  
        if (_val.length > 20) {  
            $this.val(_val.substring(0, 20));  
        }  
        count = 20 - $this.val().length;  
        $("#text-count").text(count);  
    });  
</script>

// 限制input输入内容
        $(".dj").on("input propertychange", function () {
            this.value = this.value.replace(/[^\d.]/g, '');
        });

// 获取radio选中的值
http://blog.csdn.net/htofly/article/details/7721858
1.获取选中值，三种方法都可以：
$('input:radio:checked').val()；
$("input[type='radio']:checked").val();
$("input[name='rd']:checked").val();

// 获取checkbox选中的值
            var chk_value = [];
            $('input[name="SXF"]:checked').each(function () {
                chk_value.push($(this).val());
            });
            alert(chk_value.length == 0 ? '你还没有选择任何内容！' : chk_value);

var text = $("input:checkbox[name='PutCarMan']:checked").map(function (index, elem) {
                    return $(elem).val();
                }).get().join(',');

// 手动启动或隐藏模态框。
$('#myModal').modal('toggle')

// 手动打开一个模态框。
$('#myModal').modal('show')

// 手动隐藏一个模态框。
$('#myModal').modal('hide')

// ajax
http://www.cnblogs.com/mingmingruyuedlut/archive/2011/10/18/2216553.html

// 监测代码
System.Diagnostics.Stopwatch stopwatch = new Stopwatch();
stopwatch.Start(); //  开始监视代码运行时间
// 需要测试的代码 ....
stopwatch.Stop(); //  停止监视
TimeSpan timespan = stopwatch.Elapsed; //  获取当前实例测量得出的总时间
double hours = timespan.TotalHours; // 总小时
double minutes = timespan.TotalMinutes;  // 总分钟
double seconds = timespan.TotalSeconds;  //  总秒数
double milliseconds = timespan.TotalMilliseconds;  //  总毫秒数

// linq语句
http://blog.csdn.net/hb0746/article/details/40123771

// 简析.NET Core 以及与 .NET Framework的关系
http://blog.csdn.net/zhao1949/article/details/51740559

// GitHub相关
32669448+JokerGTA@users.noreply.github.com
https://github.com/JokerGTA/GTA.git
// mysql 视图添加变量
--函数 test_e 
BEGIN
return @SSAPI;
END
--函数 test_f 
BEGIN 
return @HCAPI; 
END
--函数 test_sp
BEGIN
set @HCAPI = 'http://hc.dev.fanyuanwang.cn';-- 年度保险
set @SSAPI = 'http://ss.dev.fanyuanwang.cn';-- 员工保障
select * from v_test;
END
--视图 v_test
(
SELECT
`products`.`Id` AS `Id`,
`products`.`ProductName` AS `ProductName`,
(
CASE
WHEN (
`producttypes`.`Name` LIKE '%入职体检%'
) THEN
'入职体检'
ELSE
'年度体检'
END
) AS `Type`,
(
CASE
WHEN (
`producttypes`.`Name` LIKE '%入职体检%'
) THEN
2
ELSE
1
END
) AS `OrderType`,
(
CASE
WHEN (
`products`.`FyApplyObject` LIKE '%男%'
) THEN
'男性'
WHEN (
`products`.`FyApplyObject` LIKE '%女%'
) THEN
'女性'
ELSE
'通用'
END
) AS `ApplySex`,
`producttypes`.`Name` AS `TypeName`,
(
CASE
WHEN (`products`.`Region` = 0) THEN
'全国'
WHEN (`products`.`Region` = 1) THEN
'北京市'
WHEN (`products`.`Region` = 2) THEN
'上海市'
WHEN (`products`.`Region` = 3) THEN
'深圳市'
WHEN (`products`.`Region` = 4) THEN
'广州市'
WHEN (`products`.`Region` = 5) THEN
'武汉市'
WHEN (`products`.`Region` = 6) THEN
'成都市'
ELSE
'其他地区'
END
) AS `Region`,
(
CASE
WHEN (
`producttypes`.`Name` LIKE '%入职体检%'
) THEN
concat(
`test_f` (),
`producttypes`.`Pictures`
)
ELSE
concat(
`test_f` (),
`producttypes`.`Pictures`
)
END
) AS `Pictures`,
`products`.`RetailPrice` AS `RetailPrice`,
`products`.`FYUPrice` AS `FYUPrice`,
`products`.`IsHot` AS `IsHot`,
`products`.`IsRecommend` AS `IsRecommend`,
(
CASE
WHEN (`products`.`FyIsMarrid` = 0) THEN
'已婚'
WHEN (`products`.`FyIsMarrid` = 1) THEN
'未婚'
ELSE
'通用'
END
) AS `IsMarrid`,
`products`.`AddTime` AS `CreateTime`,
(
CASE
WHEN isnull(`products`.`EditTime`) THEN
`products`.`AddTime`
ELSE
`products`.`EditTime`
END
) AS `EditTime`,
`products`.`IsDelete` AS `IsDeleted`,
`products`.`IsValid` AS `IsValid`
FROM
(
`products`
JOIN `producttypes` ON (
(
`products`.`TypeId` = `producttypes`.`Id`
)
)
)
)
UNION
(
SELECT
`ss_products`.`Id` AS `Id`,
`ss_products`.`ProductName` AS `ProductName`,
'员工保障' AS `Type`,
3 AS `OrderType`,
'通用' AS `ApplySex`,
`ss_products`.`Type` AS `TypeName`,
'无' AS `Region`,
concat(
`test_e` (),
`ss_products`.`Picture`
) AS `Picture`,
`ss_products`.`RetailPrice` AS `RetailPrice`,
`ss_products`.`FYUPrice` AS `FYUPrice`,
`ss_products`.`IsHotSale` AS `IsHot`,
`ss_products`.`IsHomePage` AS `IsRecommend`,
'通用' AS `IsMarrid`,
`ss_products`.`CreateTime` AS `CreateTime`,
(
CASE
WHEN isnull(`ss_products`.`EditTime`) THEN
`ss_products`.`CreateTime`
ELSE
`ss_products`.`EditTime`
END
) AS `EditTime`,
`ss_products`.`IsDeleted` AS `IsDeleted`,
`ss_products`.`IsValid` AS `IsValid`
FROM
`ss_products`
)

# 函数添加数据
-- 函数insert_fg_service_val
BEGIN
# 批量添加服务项数据存储过程
# 参数说明：num_limit--添加条数; rand_limit--随机数最大值(填入10即可);
# 功能说明：批量添加的服务项数据，其关联的合同及套餐的数据为现有数据随机取出的;
DECLARE i int default 1;
DECLARE a int default 1;
DECLARE b int default 1;
DECLARE c int default 1;
DECLARE contractId int default 1;
DECLARE packageId int default 1;
DECLARE packagePrice int default 1;
DECLARE packageCode varchar(64) default '';
DECLARE packageName varchar(64) default '';
DECLARE packageType varchar(64) default '';
DECLARE packagePic varchar(64) default '';

WHILE i<=num_limit do
 
set a = FLOOR(rand()*rand_limit);
set b = FLOOR(rand()*rand_limit);
set c = FLOOR(rand()*rand_limit);

SELECT Id INTO contractId from fg_contracts order by rand( ) limit 1;
SELECT 
Id,`Code`,`Name`,Price,Type,PictureName INTO packageId,packageCode,packageName,packagePrice,packageType,packagePic 
from fg_packages order by rand( ) limit 1;

INSERT into benefits_dev.fg_service values (null,DATE(NOW()),NULL,0,contractId,packageId,packageCode,CONCAT(c,b)
,packageName,packagePrice,0,25,packageType,packagePic);

set i = i + 1;
 
END WHILE;
 
END

