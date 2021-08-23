# WCWR

Web 代码书写要求（Web-Code-Writing-Requirements）

-   为了提高 Web 研发人员个人编码素养以及编码质量。
-   为了提高 Web 团队开发项目协同工作效率。
-   为了使 Web 项目后期维护成本降低。
-   Web 开发者务必遵循书写规范进行代码编写工作
-   根据使用开发语言选择对应规范
-   参考用例 demo 更快了解书写规范

## 阅读对象

所有 Web 研发人员

## 开发语言

1. JavaScript

## 项目框架

1. Vue.js [vue 项目规范示例](http://www.linwutong.com:9092/qc/WCWR-vue-demo)
2. React.js

## 命名规范

### 四种命名方法

1. 小驼峰命名法，除首单词外，其余所有单词的第一个字母大写。如：allPrice，getAllNames
2. 大驼峰命名法，所有单词的第一个字母大写。如：GuideActivity，StudentInfoBean
3. 中划线命名法:单词与单词间用中划线做间隔。如：error-log, select-background-color
4. 下划线命名法:单词与单词间用中划线做间隔。如：ERROR_LOG

## JavaScript 规范

### 常量

全部大写,采用[下划线命名法](#四种命名方法).例如：MIN_WIDTH

### 变量

声明变量时，使用 const、let 关键字, 采用[小驼峰命名法](#四种命名方法)

### 方法命名

有关 onChange, onClick, onInput 等表单元素触发的事件一律使用 handle 开头,(handleChange, handleClick, handleInput)

其余类型的事件名遵循[小驼峰命名法](#四种命名方法)

## css 规范

-   统一使用展开格式书写样式

```css
.jdc {
	display: block;
	width: 50px;
}
```

-   类名的命名应该尽量精短、明确，必须以字母开头命名，且全部字母为小写，单词之间统一使用中划线 “\-”或 “\_” 连接

## Vue.js 规范

### Vue.js 项目结构

```
        项目根目录 /
        ├── node_modules # 项目依赖
        ├── dist/    # 压缩、编译后的代码，用于生产环境
        |── public/   # 公共静态资源
        |   ├── favicon.ico    # 应用图标
        |   └── index.*        # 主页 html 模板
        |── src/               # 源代码
        |   ├── api/           # 接口请求管理
        |   |   └── <A模块>.js  # A模块所有接口请求
        |   |   └── <B模块>.js  # B模块所有接口请求
        |   ├── assets/        # 项目图片,音视频静态资源
        |   |   └── A模块/      # A模块所有资源的文件夹
        |   |   └── B模块/      # B模块所有资源的文件夹
        |   ├── components/    # 项目公用组件
        |   |   └── 公用组件A/  # 公用组件A
        |   |       └── index.vue  # 公用组件A入口
        |   |   └── 公用组件B/  # 公用组件B
        |   |       └── index.vue  # 公用组件B入口
        |   ├── filters/       # 过滤器
        |   ├── directive/     # 自定义指令
        |   ├── plugins/       # 插件
        |   ├── utils/         # 工具组件
        |   ├── layout/        # 页面整体布局
        |   ├── constant/      # 常量
        |   ├── views/         # 页面组件
        |   |   └── A模块/      # A模块所有页面与A模块组件
        |   |   └── B模块/      # B模块所有页面与A模块组件
        |   ├── router/        # 路由管理
        |   ├── styles/        # 公共样式
        |   ├──  └── element-variables.scss  # 例如覆盖element-ui的样式文件
        |   ├──  └── index.scss  # 汇总所有样式
        |   ├── store/         # vuex状态管理
        |   |   └── index.js   # vuex入口文件
        |   |   └── modules/   # 所有模块文件夹
        |   |      └── <A模块>.js   # A模块的所有状态管理
        |   └── App.vue        # 根组件
        |   └── main.js        # 入口文件
        |──  (babel.config.js | .babelrc)  # babel  编译配置
        |── .eslintrc.*    # eslint 代码规则检查配置
        |── .prettierrc.*   # prettier 代码格式化配置
        |── vue.config.js   # webpack工程配置
        |── .browserslistrc   # 浏览器兼容配置
        |── .editorconfig   # 格式化配置
        |── jsconfig.json   # vscode路径别名配置
        |── package.json    # npm信息配置
        |── package-lock.json    # npm包版本锁定配置
        |── postcss.config.js    # css处理配置
        |── .env.*    # vuecli环境变量配置
```

### Vue 项目目录命名规范

#### component

所有公共组件(components 文件夹下)命名以使用[大驼峰命名法](#四种命名方法)进行命名

#### views

views 文件夹下所有模块文件夹命名以使用[中划线命名法](#四种命名方法)进行命名

**其余 Vue 项目的命名规则按照 [vue 项目规范示例](http://www.linwutong.com:9092/qc/WCWR-vue-demo) 项目为准**

#### Vue 项目编写规范(优先级 A 和 B 必须遵守)

引用自 Vue 官方: https://cn.vuejs.org/v2/style-guide/index.html#%E8%A7%84%E5%88%99%E5%BD%92%E7%B1%BB

## React.js 规范

### React.js 项目结构

    项目根目录
    ├── build/    # 压缩、编译后的代码，用于生产环境
    ├── docs/     # 项目文档
    |── config/   # 开发环境配置
    |   |── nginx.conf            # nginx 服务器配置
    |   ├── path.config.js        # 项目路径配置
    |   ├── webpack.config.js     # webpack 配置
    |   ├── webpack.dll.config.js # webpack 外部依赖配置
    |   ├── devServer.config.js   # 开发服务器配置
    |   ├── jest.config.js        # jest  代码测试配置
    |── public/   # 公共静态资源
    |   ├── manifest.json         # 应用图标，名称信息
    |   └── index.(html|ejs)      # 主页 html 模板
    |── scripts/  # 脚本
    |   └── start.js       # 启动脚本
    |── src/      # 源代码
    |   ├── components/    # 组件
    |   |   └── shared/    # 公共组件
    |   |   └── auth-control(模块文件夹)/       # [中划线命名法](#四种命名方法)
    |   ├── models/        # redux 配置文件
    |   ├── apis/          # 后端接口请求
    |   ├── utils/         # 工具组件、常量
    |   ├── assets/        # 静态资源
    |   ├── vendors/       # 外部依赖
    |   ├── index.js       # 主入口文件
    |   └── index.scss
    |── .babelrc.js       # babel  编译配置
    |── .eslintrc.json    # eslint 代码规则检查配置
    |── .prettierrc.yml   # prettier 代码格式化配置
    |── tsconfig.json     # typescript 配置文件

#### 按功能或路由组织 {#grouping-by-features-or-routes}

-   组织项目文件结构的一种常见方法是将 CSS、JS 和测试文件一起按照功能或路由进行组织。

```
common/
  Avatar.js
  Avatar.css
  APIUtils.js
  APIUtils.test.js
feed/
  index.js
  Feed.js
  Feed.css
  FeedStory.js
  FeedStory.test.js
  FeedAPI.js
profile/
  index.js
  Profile.js
  ProfileHeader.js
  ProfileHeader.css
  ProfileAPI.js
```

#### 按文件类型组织 {#grouping-by-file-type}

-   另一种组织项目文件结构的常用方法是将类似的文件组织在一起，例如：

```
api/
  APIUtils.js
  APIUtils.test.js
  ProfileAPI.js
  UserAPI.js
components/
  Avatar.js
  Avatar.css
  Feed.js
  Feed.css
  FeedStory.js
  FeedStory.test.js
  Profile.js
  ProfileHeader.js
  ProfileHeader.css
```

#### 避免多层嵌套

-   单个项目中的目录嵌套控制在最多四个层级内。

### 命名规范

-   组件文件扩展名

如果使用 JavaScript，则文件扩展名为 `.js`；如果使用 `TypeScript`，则文件扩展名为 `.tsx`

-   组件文件名

如果是组件文件，则使用[大驼峰命名法](#四种命名方法)，如 `MyComponent.js`

如果组件是一个目录，则组件主入口命名为 `index`，如 `index.js`

-   引用命名

React 组件使用 [大驼峰命名法](#四种命名方法)

```jsx
// 反例
import reservationCard from './ReservationCard'

// 好的做法
import ReservationCard from './ReservationCard'
```

-   组件命名

使用文件名作为组件名字，例如, `ReservationCard.js` 应该包含名为 `ReservationCard` 的引用，然而对于文件夹中的根组件, 使用 `index.js` 作为文件名，使用文件夹的名字作为组件的名字

```jsx
// 反例
import Footer from './Footer/Footer'

// 反例
import Footer from './Footer/index'

// 好的做法
import Footer from './Footer'
```

-   组件属性名

React DOM 使用[小驼峰命名法](#四种命名方法)来定义属性的名称，而不使用 HTML 属性名称的命名约定，例如

```jsx
<div onClick={this.handleChange} />
```

### 类组件 VS 函数式组件

只允许使用 `Class Component` 和 `Functional Component` 两种形态来书写组件，建议尽量使用函数式组件配合 Hooks 来进行开发

### 对齐

遵循以下 JSX 语法的对齐风格

```jsx
// 反例
<Foo superLongParam='bar'
     anotherSuperLongParam='baz' />

// 好的做法
<Foo
  superLongParam='bar'
  anotherSuperLongParam='baz'
/>

// 反例
{showButton &&
  <Button />
}

// 反例
{
  showButton &&
    <Button />
}

// 好的做法
{showButton && (
  <Button />
)}

// 好的做法
{showButton && <Button />}
```

### 空格

-   自闭合的标签前要加一个空格

```jsx
//反例
<Foo/>

// 反例
<Foo/>
<Foo                 />

// 反例
<Foo
 />

// 好的做法
<Foo />
```

### 属性

-   属性名使用[小驼峰命名法](#四种命名方法)

```jsx
// 反例

<Foo
  UserName='hello'
  phone_number={12345678}
/>

// 好的做法
<Foo
  userName='hello'
  phoneNumber={12345678}
/>
```

### 圆括号

当 JSX 标签超过一行时使用圆括号包裹

```jsx

// 反例
render () {
  return <MyComponent className='long body' foo='bar'>
           <MyChild />
         </MyComponent>
}

// 好的做法
render () {
  return (
    <MyComponent className='long body' foo='bar'>
      <MyChild />
    </MyComponent>
  )
}

// 当只有一行时, 好的做法
render () {
  const body = <div>hello</div>
  return <MyComponent>{body}</MyComponent>
}
```

### 方法

-   类组件的内部方法不要使用下划线前缀

```jsx
// 反例
class extends React.Component {
  _onClickSubmit () {
    // todo
  }

   // todo
}

// 好的做法
class extends React.Component {
  onClickSubmit () {
    // todo
  }

   // todo
}
```
