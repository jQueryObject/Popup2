# jquery弹出框2Popup2
效果如下：
![](image/img.gif)

all code:
```
<!doctype html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>jQuery实现的很炫很酷的弹出层效果</title>
    <link rel="stylesheet" href="css/common.css"/>
    <style>
        .zxx_list_title{background:#eeeeee; border:1px solid #cccccc; padding:1em;}
        .zxx_list_content{padding:1em;}
        #tinybox{position:absolute; display:none; padding:10px; background:#ffffff url(image/preload.gif) no-repeat 50% 50%; border:10px solid #e3e3e3; z-index:2000;}
        #tinymask{position:absolute; display:none; top:0; left:0; height:100%; width:100%; background:#000000; z-index:1500;}
        #tinycontent{background:#ffffff; font-size:1.1em;}
    </style>
</head>
<body>
<div class="zxx_out_box">
    <div class="zxx_in_box">
        <h3 class="zxx_title">jQuery实现很炫很酷的弹出层效果</h3>
        <div class="zxx_main_con">
            <div class="zxx_list_title"><b>加载一个静态页面</b><a class="ml20" href="#zhangxinxu" id="click_test1">效果预览</a></div>
            <div class="zxx_list_content">加载一个静态页面，这里可能无法测试出来，在服务器项目里可以看见效果</div>
            <div class="zxx_list_title"><b>图片</b><a class="ml20" href="#zhangxinxu" id="click_test2">效果预览</a></div>
            <div class="zxx_list_content">用酷酷的浮动层显示图片</div>
            <div class="zxx_list_title"><b>显示flash</b><a class="ml20" href="#zhangxinxu" id="click_test3">效果预览</a></div>
            <div class="zxx_list_content">用酷酷的浮动层显示flash</div>
            <div class="zxx_list_title"><b>自动隐藏</b><a class="ml20" href="#zhangxinxu" id="click_test4">效果预览</a></div>
            <div class="zxx_list_content">层显示一段时间后自动隐藏，当作操作提示用是个很不错的选择</div>
        </div>
    </div>
</div>
</body>
</html>
<script src="js/tinybox.js"></script>
<script>
    T$('click_test1').onclick = function(){TINY.box.show('blank-for-test.html',1,300,150,1)};
    var content2 = "<img width='640' height='466' src='http://image.zhangxinxu.com/image/study/s/mm10.jpg' />";
    T$('click_test2').onclick = function(){TINY.box.show(content2,0,0,0,1)};
    var content3 = "<object classid='clsid:D27CDB6E-AE6D-11cf-96B8-444553540000' width='550' height='400'><param name='movie' value='flash/as3_clock_2.swf' /><param name='quality' value='high' /><param name='wmode' value='opaque' /><embed height='400' width='550'  src='flash/as3_clock_2.swf' type='application/x-shockwave-flash'></embed></object>";
    T$('click_test3').onclick = function(){TINY.box.show(content3,0,0,0,1)};
    var content4 = "该浮动层将在3秒钟内消失。";
    T$('click_test4').onclick = function(){TINY.box.show(content4,0,0,0,0,3)}
</script>








```

