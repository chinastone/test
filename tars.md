cywin 安装使用

> 报错 `missing: ZLIB_LIBRARY ZLIB_INCLUDE_DIR`

> 运行时加上路径配置 
>
> ```shell
> cmake .. -DZLIB_INCLUDE_DIR=/usr/i686-pc-cygwin/sys-root/usr/include  -DZLIB_LIBRARY=/usr/i686-pc-cygwin/sys-root/usr/lib cls
> ```



