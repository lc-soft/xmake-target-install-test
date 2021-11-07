# xmake-target-install-test

XMake 的 target:install 测试项目。

问题复现步骤：

```bash
cd libadd

# 构建并打包 libadd
xmake package

cd test

# 构建 libadd 的测试程序
xmake -P .

# 运行测试程序（没有报错 libadd.dll 找不到，似乎 xmake 有做特殊处理）
xmake run -P . test

# 安装测试程序
xmake install -P . -o install

```

最后，检查 libadd/test/install/bin 目录是否有 libadd.dll 文件。
