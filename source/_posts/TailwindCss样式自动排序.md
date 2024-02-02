---
title: TailwindCss样式自动排序
date: 2024-02-02 11:31:40
tags:
---

# TailwindCss 样式自动排序 prettier-plugin-tailwindcss

tailwind CSS 的 Prettier 插件，可根据官方推荐的类顺序自动对类进行排序。

1.安装 prettier 包

`npm i prettier -D`

2.在项目根目录下创建 .prettierrc.cjs 文件，用于自设置美化格式

`// prettier.config.js`

`module.exports = {`

`plugins: ["prettier-plugin-tailwindcss"],`

`tailwindConfig: "./tailwind.config.js",`

`};`

3.安装 prettier-plugin-tailwindcss

`npm install -D prettier-plugin-tailwindcss`

4.设置 tailwind.config.js

`/** @type {import('tailwindcss').Config} */`

`module.exports = {`

`content: ["./src/**/*.{vue,js,ts,jsx,tsx}"],`

`theme: {`

`extend: {},`

`},`

`plugins: ["prettier-plugin-tailwindcss"],`

`};`

5.一旦你完成了安装和配置，你可以使用以下命令来运行 Prettier 格式化你的代码：

`npx prettier --write .prettierrc.cjs`

这样，你的代码将会根据`.prettierrc.js`文件中的配置选项来进行格式化。如果以后你修改了`.prettierrc.js`文件中的选项，只需要再次运行上述命令即可保持格式一致。
