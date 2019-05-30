# tagTree
树型标签选择器

该控件是基于jquery库开发的，所以使用前，必需引入这些库。
同时选择勾勾为字体库图标，如果不想引入图标字体库，可以自己改成图片。
该控件是一个树型选择器，支持多选单选，并返回值。

# 初始化方法

## 定义控件
```html
<div id="test"></div>
```

## 控件数据结构
```json
var data =[
	    {
	    	name:"1号标签",
	    	value:"1",
	    	children:[
	    		{
	    			name:"11号标签",
			    	value:"11",
			    	children:[]
	    		},
				{
	    			name:"12号标签",
			    	value:"12",
			    	children:[]
	    		},
				{
	    			name:"13号标签",
			    	value:"13",
			    	children:[
			    		{
			    			name:"131号标签",
					    	value:"131",
					    	children:[]
	    				}
	    			]
	    		}
	    	]
	    },
	    {
	    	name:"2号标签",
	    	value:"2",
	    	children:[
	    		{
	    			name:"21号标签",
			    	value:"21",
			    	children:[]
	    		},
				{
	    			name:"22号标签",
			    	value:"22",
			    	children:[]
	    		}
	    	]
	    },
	    {
	    	name:"3号标签",
	    	value:"3",
	    	children:[]
	    }
    ];
```

## 初始化控件数据
```javascript
$("#test").tagTree({
    	id:"",
    	data:data,
    	fold:false,
    	multiple:false,
    	check:function(val){
    		console.log('chekc:'+val);
    		console.log($(this).tagTreeValues());
    	},
    	done:function(){
    		console.log('tagTree is ok!');
    	}
    });
```

## 运行效果如下
![image](https://github.com/miracleren/tagTree/blob/master/img/show.png)
