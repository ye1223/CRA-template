## Create-React-App项目Template初始化项目

​	`yarn add create-react-app [app-name] --template typescript`

### prettier

​	`yarn add -D prettier`

```js
//prettier.config.js
module.exports = {
   semi: false, // 在每条语句的末尾不使用分号
   trailingComma: 'es5', // 允许在ES5中有效的尾随逗号
   singleQuote: true, // 使用单引号而不是双引号
   printWidth: 80, // 指定打印行的最大长度
   tabWidth: 3, // 设置每个缩进级别的空格数
   useTabs: false, // 使用空格而不是制表符进行缩进
   bracketSpacing: true, // 在对象字面量中添加空格
   jsxBracketSameLine: false, // 在JSX中把'>'放在最后一行的末尾
   arrowParens: 'avoid', // 当箭头函数只有一个参数时不使用圆括号
   endOfLine: 'lf', // 行尾序列使用LF（\n）
}
```



### ESLint

```
yarn add -D eslint
npx eslint --init
```

### **husky**

​	`yarn add -D husky`

```json
//package.json
"scripts": {
  "prettier": "prettier --write \"src/**/*.{js,jsx,ts,tsx,json,css,scss,md}\""
}
```

​	**启用 Git 钩子**： `npx husky install`

​	**添加 pre-commit 钩子**：`npx husky add .husky/pre-commit "yarn prettier"` （eslint还没写，因为不想用）

### 路径别名

```json
"compilerOptions": {
  // ...其他配置...
  "baseUrl": "src",
  "paths": {
    "@/*": ["*"]
  }
}
```



# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `yarn start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

### `yarn test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `yarn build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `yarn eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).
