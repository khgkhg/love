<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN">
<html>
  <head>
    <base href="<%=basePath%>">
    <link rel="icon" href="<%=path%>/link.jpg" type="image/x-icon">
    <title>2016-05-04 23:46:00 </title>
	<meta http-equiv="pragma" content="no-cache">
	<meta http-equiv="cache-control" content="no-cache">
	<meta http-equiv="expires" content="0">    
	<meta http-equiv="keywords" content="keyword1,keyword2,keyword3">
	<meta http-equiv="description" content="This is my page">
	<!--
	<link rel="stylesheet" type="text/css" href="styles.css">
	-->
  </head>
  
  <body>
    
	<div style="width:100%;height:100%;background-image: url(https://pan.baidu.com/s/15GiUp_0VDc0MR6CtsQKfng);background-repeat: no-repeat;background-size: 100% 95%;">
	  <div style="text-align:center;height:200px;width:630px;border: 2px solid #eee; position: absolute;left: 7%;top: 200px;background-color:rgba(236, 137, 137, 0.39);">
		<h2 id="day">今天是我们的第天</h2>
		<h2 id="timestring">xxx年 xx月 xx日 23小时 56 分</h2>
	  </div>
	</div>
    <script>   
    var arr = "2016/05/04 23:46:00".split(/[- : \/]/);
    var begintime = new Date(arr[0],arr[1]-1,arr[2],arr[3],arr[4],arr[5]);
  	var oneyear = 365*24*3600;
  	var onemonth = 30*24*3600;
  	var oneday = 24*3600;
  	var onehour = 3600;
  	var oneminute = 60;
  	var onesecond = 1;
  	
    function myInterval (){
    	  var nowtime = new Date(); 
    	//  console.log(begintime);
    	  var overtimeLong =parseInt ( (nowtime.getTime() - begintime.getTime())/1000 );// 秒级
    	  var year = 0;
    	  var month = 0;
    	  var day = 0;
    	  var hour = 0;
    	  var minute = 0;
    	  var second = 0;
    	  var allDay = 0 ;
    	  allDay =parseInt( overtimeLong / oneday ) +1 ;
    	  
    	   year =parseInt( overtimeLong / oneyear ) ;
    	  if (year > 0 ){
    		  overtimeLong = overtimeLong - (oneyear * year ) ;
    	  }
    	  month = parseInt( overtimeLong / onemonth );
    	  if (month > 0 ){
    		  overtimeLong = overtimeLong - (onemonth * month ) ;
    	  }
    	   day = parseInt ( overtimeLong / oneday );
    	  if ( day  > 0 ) {
    		  overtimeLong = overtimeLong - (oneday * day );
    	  }
    	   hour = parseInt ( overtimeLong / onehour );
    	  if ( hour  > 0 ) {
    		  overtimeLong = overtimeLong - (onehour * hour );
    	  }
    	   minute = parseInt ( overtimeLong / oneminute );
    	  if ( minute  > 0 ) {
    		  overtimeLong = overtimeLong - (oneminute * minute );
    	  }
    	   second = overtimeLong ;
    	   var timeString = "一起度过了";//xxx年 xx月 xx日 23小时 56 分
    	   var allDayString = "今天是我们的第";
    	   allDayString +=" <span style='color:#fff;background-color: #FFC107;font-size: 40px;'>"+allDay+"</span> 天";
    	   timeString +=" <span style='color:#fff;background-color: #FFC107;font-size: 32px;'>"+year+"</span> 年 ";
    	   timeString +=" <span style='color:#fff;background-color: #FFC107;font-size: 32px;'>"+month+"</span> 月";
    	   timeString +=" <span style='color:#fff;background-color: #FFC107;font-size: 32px;'>"+day+"</span> 日";
    	   timeString +=" <span style='color:#fff;background-color: #FFC107;font-size: 32px;'>"+hour+"</span> 小时";
    	   timeString +=" <span style='color:#fff;background-color: #FFC107;font-size: 32px;'>"+minute+"</span> 分钟";
    	   timeString +=" <span style='color:#fff;background-color: #FFC107;font-size: 32px;'>"+second+"</span> 秒";
    	   document.getElementById('timestring').innerHTML=timeString;
    	   document.getElementById('day').innerHTML=allDayString;
    };
    		myInterval();
          setInterval("myInterval()",1000);//1000为1秒钟
    </script>
  </body>
</html>
