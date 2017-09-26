# jQuery.html5upload.js
基于jQuery和HTML5实现的带进度监控的文件上传插件

## OPTIONS

fileTypeExts:允许上传的文件类型 用,隔开 jpg,png

url:文件上传的地址

auto:是否选择文件后就进行上传

multi:是否支持文件多选

formData:除文件外的POST数据

fileObjName:文件的filedName

fileSizeLimit:所有文件的总大小上传限制

queueSizeLimit:最多可选择的文件数量

onSelect:选择文件后的回调函数

onUploadStart:上传开始时的回调函数

onUploadProgress:进度监控的回调函数

onUploadSuccess:上传成功后的回调函数

onUploadComplete:上传完成后(不管成功和失败都执行)的回调函数

onUploadError:上传失败后的回调函数

onInit:插件初始化的回调函数

onCancel:取消文件上传的回调函数

## DEMO

### 上传插件初始化
```js
$("#button").h5upload(function(){
  url:'/uploadFile',
	fileObjName:'upload',
	fileSizeLimit:500*1024*1024,
	formData:{},
	onSelect:function(file){
		
	},
	onUploadProgress:function(file,uploaded,total){
				
	},
	onUploadSuccess:function(file,data){
		
	},
	onUploadError:function(file){
		
	}
});
```
### 取消上传
```js
$("#button").h5upload("cancel",file.id);  //单个文件取消上传
$("#button").h5upload("cancel");  //全部取消上传
```

