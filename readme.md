** 路径中不要有中文

## 项目描述 
所有开发程序的静态文件，上传到vercel服务器。

## 项目搭建  
启动 wsl
conda create -n vercel_fastapi_env python=3.9
conda activate vercel_fastapi_env
pip install fastapi
pip install "uvicorn[standard]"

## 项目启动  
conda activate vercel_fastapi_env

## 程序运行逻辑 
本地 启动 python main.py 看到结果
vercel抓取github的repo，根据vercel.json的配置，启动项目


## 开发  
每次把静态文件放入static，*路径千万不要有中文*
如果装了新包，要运行 pip freeze > requirements.txt
在github（biodancerApi）网页上修改该repo，然后上传更新。
在vercel网页上选择repo，之后不需要更新，一旦github更新，vercel自动抓取。

## 测试  
本地: http://127.0.0.1:8000/新标日初级上mp3/1.1.aac 访问成功
远程: