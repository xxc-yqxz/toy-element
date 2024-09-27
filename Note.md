```
echo -e 'packages:\n - "packages/*"' > pnpm-workspace.yaml
```

这条命令的作用是创建一个名为`pnpm-workspace.yaml`的文件，并向其中写入特定的内容。

具体来说，写入的内容为：

```yaml
packages:
 - "packages/*"
```

在使用`pnpm`进行包管理时，这个文件通常用于定义工作空间（workspace）。其中，`packages`字段指定了工作空间中的包的路径。在这个例子中，`- "packages/*"`表示将`packages`目录下的所有内容都视为工作空间中的包。

这可以让`pnpm`在安装和管理依赖时，能够自动识别和处理这些包之间的依赖关系，从而提高开发效率和代码的可维护性。


```shell
for i in components core docs hooks theme utils; do
 cd $i
 pnpm init
 cd ..

done


pnpm create vite play --template vue-ts
```

