# RQC 说明

index.html 中 Google tag 是 google 的统计代码。


### 开发：

pnpm install

pnpm dev

### 发布：

pnpm build

### 错误处理

如果提示错误：Could not find a declaration file for module 'lodash'. 

执行命令：

pnpm i --save-dev @types/lodash

然后再执行。

### 打包后的静态文件部署到子目录网站空白

原因是静态文件路径从 /assets/ 开始，而不是 ./assets/

解决方案：修改 vite.config.ts 加上 base: './' 发布后正常。

```
export default defineConfig({  
  ...,
  base: './',  
  ...
})
```