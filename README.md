### 这是一个简易的electron开发的脚手架，虽然里面用的vue，但是改成react或者其他框架都很容易的


1. 开发: (开发模式只需要用到app目录就可以了)
```
cd app
yarn 
yarn start
```

2. 打包：（在最外层目录）
```
yarn 
yarn app
```
3. 注意打包的时候，终端必须科学上网
```
cmd下配置
set http_proxy=http://127.0.0.1:xxx
set http_proxys=http://127.0.0.1:xxx

重置
set http_proxy=
set http_proxys=

gitbash/shell下配置

export http_proxy=http://127.0.0.1:xxx
export https_proxys=http://127.0.0.1:xxx

重置
export http_proxy=
export http_proxys=

```