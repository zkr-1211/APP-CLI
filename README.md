# 学习搭建cli脚手架

## 安装
### 全局安装
$ npm install -g zkr-cli-test
# or yarn
$ yarn global add zkr-cli-test

### 借助npx
创建模版
$ npx create zkr-cli <name> [-t|--template]
示例
$ npx create zkr-cli hello-cli -template vue3-vant-mobile

## 使用
创建模版
$ zkr-cli create <name> [-t|--template]
示例
$ zkr-cli create hello-cli -t vue3-vant-mobile


## 关于npm（如何发布自己的npm包）可参考 https://zhuanlan.zhihu.com/p/575485165

## 登录npm
npm login --registry https://registry.npmjs.org

## 发布npm
npm publish --registry https://registry.npmjs.org

## 后续更新npm包
npm version patch
  npm version后面参数说明：
    patch：小变动，比如修复bug等，版本号变动 v1.0.0->v1.0.1
    minor：增加新功能，不影响现有功能,版本号变动 v1.0.0->v1.1.0
    major：破坏模块对向后的兼容性，版本号变动 v1.0.0->v2.0.0

## 迭代版本号之后重复第四步
npm publish --registry https://registry.npmjs.org

## 撤销发布（慎用）
npm unpublish 包名@版本号 --force （根据需要接上npm源地址）
示例：npm unpublish mikey-npm-test@1.0.0 --force --registry https://registry.npmjs.org