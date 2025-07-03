---
title: 'Markdown 常用标记语言'
authors: ['default']
date: '2024-12-07'
lastmod: '2025-04-07'
tags: ['Markdown', '知识库']
draft: false
layout: PostLayoutFull
summary: 'Markdown 常用标记语言集合。'
---

## 目录

<TOCInline toc={props.toc} exclude="Introduction" />

```Text:PageTitle
<TOCInline toc={props.toc} exclude="Overview" toHeading={2} />

<TOCInline toc={props.toc} exclude="Introduction" />

<TOCInline toc={props.toc} asDisclosure />
```

---

## 资料

- [Next.js Starter Blog](https://tailwind-nextjs-starter-blog.vercel.app)
- [Internationalization (i18n) Routing](https://nextjs.org/docs/pages/building-your-application/routing/internationalization)
- [Supported Functions · KaTeX](https://katex.org/docs/supported.html)
- [Deriving the OLS Estimator | Next.js Starter Blog](https://tailwind-nextjs-starter-blog.vercel.app/blog/deriving-ols-estimator)
- [Front matter | Hugo](https://gohugo.io/content-management/front-matter/)
- [Fontsource](https://fontsource.org)
  - Install the preferred [font](https://fontsource.org/fonts) - `npm install -save @fontsource/<font-name>`
  - Update the import at `pages/_app.js`- `import '@fontsource/<font-name>.css'`
  - Update the `fontfamily` property in the tailwind css config file

---

## 文本块

- **邮件订阅入口**
  <BlogNewsletterForm title="Like what you are reading?" />

```jsx:BlogNewsletterForm.tsx
<BlogNewsletterForm title="Like what you are reading?" />
```

- [链接文本](https://www.example.com)

```Text:链接文本
[链接文本](https://www.example.com)
```

- **加粗文本**

```Text:加粗文本
**加粗文本**

__加粗文本__
```

- **斜体文本**：_斜体文本_ _斜体文本_

```Text:斜体文本
*斜体文本*

_斜体文本_
```

- **加删除线**：~~加删除线文本~~

```Text:加删除线
~~加删除线文本~~
```

- **脚注**：这是一个带有脚注的句子[^1]。

```Text:脚注
这是一个带有脚注的句子[^1]。
```

- **引用块**：
  > 这是一个引用块。

```Text:引用块
> 这是一个引用块。
```

- **警告提示**
  > [!CAUTION]

```Text:警告提示
> [!CAUTION]
```

- **列表**
  - 子项目1
  * 子项目2
  - 子项目3

```Text:列表
- **列表**
  - 子项目1
  * 子项目2
  + 子项目3
```

- **任务**
- [x] 任务1
- [ ] 任务2

```Text:任务
- [x] 任务1
- [ ] 任务2
```

- **表格**

| 表头1 | 表头2 |
| ----- | ----- |
| 内容1 | 内容2 |
| 内容3 | 内容4 |

```Text:表格
| 表头1 | 表头2  |
| ----- | ----- |
| 内容1 | 内容2  |
| 内容3 | 内容4  |
```

- **标题**

```Text:标题
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题
```

- **参考书目和引文 （v1.2.1）**：[timlrx/rehype-citation](https://github.com/timlrx/rehype-citation)

Standard citation [^Nash1950]

[^Nash1950]: Nash, J. (1950). _Equilibrium points in n-person games._ Proceedings of the National Academy of Sciences, 36(1), 48-49.

```Text:参考书目和引文
Standard citation [^Nash1950]

[^Nash1950]: Nash, J. (1950). *Equilibrium points in n-person games.* Proceedings of the National Academy of Sciences, 36(1), 48-49.

```

---

## 代码块

- [Basic writing and formatting syntax - GitHub Docs](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

- **内嵌代码**：`Code`、<code>selectAll()</code>、`print("Hello, World!")`

```Text:code.txt
`Code`
<code>selectAll()</code>
`print("Hello, World!")`
```

- **Bash**

```Bash:bash.sh
npm start
# or
npm run dev
```

- **CSS**

```CSS:style.css
.code-highlight {
  @apply float-left min-w-full;
}

.code-line {
  @apply border-opacity-0 -mx-4 block border-l-4 pr-4 pl-4;
}

.code-line.inserted {
  @apply bg-opacity-20 bg-green-500;
}

.code-line.deleted {
  @apply bg-opacity-20 bg-red-500;
}

.highlight-line {
  @apply border-primary-500 bg-opacity-50 -mx-4 border-l-4 bg-gray-700;
}

.line-number::before {
  @apply mr-4 -ml-2 inline-block w-4 text-right text-gray-400;
  content: attr(line);
}
```

- **Python**

```Python:sum.py
def fib():
    a, b = 0, 1
    while True:            # First iteration:
        yield a            # yield 0 to start with and then
        a, b = b, a + b    # a will now be 1, and b will also be 1, (0 + 1)

for index, fibonacci_number in zip(range(10), fib()):
     print('{i:3}: {f:3}'.format(i=index, f=fibonacci_number))
```

- **Javascript**

```Javascript:sum.js
var num1, num2, sum
num1 = prompt('Enter first number')
num2 = prompt('Enter second number')
sum = parseInt(num1) + parseInt(num2) // "+" means "add"
alert('Sum = ' + sum) // "+" means combine into a string
```

```Javascript:sum.js {1,3-4} showLineNumbers
var num1, num2, sum
num1 = prompt('Enter first number')
num2 = prompt('Enter second number')
sum = parseInt(num1) + parseInt(num2) // "+" means "add"
alert('Sum = ' + sum) // "+" means combine into a string
```

```js:siteMetadata.js
analytics: {
    // supports plausible, simpleAnalytics or googleAnalytics
    plausibleDataDomain: '', // e.g. tailwind-nextjs-starter-blog.vercel.app
    simpleAnalytics: false, // true or false
    googleAnalyticsId: '', // e.g. UA-000000-2 or G-XXXXXXX
  },
```

```diff-js:siteMetadata.js
// 删除和加亮
analytics: {
-   umamiAnalytics: {
-     // We use an env variable for this site to avoid other users cloning our analytics ID
-     umamiWebsiteId: process.env.NEXT_UMAMI_ID, // e.g. 123e4567-e89b-12d3-a456-426614174000
-   },
+    plausibleAnalytics: {
+      plausibleDataDomain: '', // e.g. tailwind-nextjs-starter-blog.vercel.app
+    },
},
```

- **Javascript XML**

```jsx:PageTitle.tsx
// Or import PageTitle from './components/PageTitle.js' if you are using js
import PageTitle from './components/PageTitle.tsx'
;<PageTitle> Using JSX components in MDX </PageTitle>
```

- **TypeScript**

```tsx:DonutChart.tsx
'use client'

import { Doughnut } from 'react-chartjs-2'
import { Chart as ChartJS, ArcElement, Tooltip, Legend } from 'chart.js'

ChartJS.register(ArcElement, Tooltip, Legend)

const DonutChart = ({ data }) => {
  return <Doughnut data={data} />
}

export default Doughnut
```

```ts:contentlayer.config.ts
export const Blog = defineDocumentType(() => ({
  name: 'Blog',
  filePathPattern: 'blog/**/*.mdx',
  contentType: 'mdx',
  fields: {
    title: { type: 'string', required: true },
    date: { type: 'date', required: true },
    tags: { type: 'list', of: { type: 'string' }, default: [] },
    ...
  },
  computedFields: {
    readingTime: { type: 'json', resolve: (doc) => readingTime(doc.body.raw) },
    slug: {
      type: 'string',
      resolve: (doc) => doc._raw.flattenedPath.replace(/^.+?(\/)/, ''),
    }
    ...
  },
}))
```

---

## 内容嵌入块

- 在线图片嵌入链接 [![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/git/external?repository-url=https://github.com/timlrx/tailwind-nextjs-starter-blog)

```Image:favicon.ico
[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/git/external?repository-url=https://github.com/timlrx/tailwind-nextjs-starter-blog)
```

- 本地图片（定义大小）
  <Image alt="favicon" src="/static/favicons/favicon.ico" width={100} height={100} />

```Image:favicon.ico
<Image alt="favicon" src="/static/favicons/favicon.ico" width={100} height={100} />
```

- 本地图片（自适应）
  ![favicon](/static/favicons/favicon.ico)

```Image:favicon.ico
![favicon](/static/favicons/favicon.ico)
```

- 本地图片并排
  <div className="-mx-2 flex flex-wrap overflow-hidden xl:-mx-2">
    <div className="my-1 w-full overflow-hidden px-2 xl:my-1 xl:w-1/2 xl:px-2">
      ![favicon](/static/favicons/favicon.ico)
    </div>
    <div className="my-1 w-full overflow-hidden px-2 xl:my-1 xl:w-1/2 xl:px-2">
      ![favicon](/static/favicons/favicon.ico)
    </div>
    <div className="my-1 w-full overflow-hidden px-2 xl:my-1 xl:w-1/2 xl:px-2">
      ![favicon](/static/favicons/favicon.ico)
    </div>
    <div className="my-1 w-full overflow-hidden px-2 xl:my-1 xl:w-1/2 xl:px-2">
      ![favicon](/static/favicons/favicon.ico)
    </div>
  </div>

```html:favicon.ico
  <div className="-mx-2 flex flex-wrap overflow-hidden xl:-mx-2">
    <div className="my-1 w-full overflow-hidden px-2 xl:my-1 xl:w-1/2 xl:px-2">
      ![favicon](/static/favicons/favicon.ico)
    </div>
    <div className="my-1 w-full overflow-hidden px-2 xl:my-1 xl:w-1/2 xl:px-2">
      ![favicon](/static/favicons/favicon.ico)
    </div>
    <div className="my-1 w-full overflow-hidden px-2 xl:my-1 xl:w-1/2 xl:px-2">
      ![favicon](/static/favicons/favicon.ico)
    </div>
    <div className="my-1 w-full overflow-hidden px-2 xl:my-1 xl:w-1/2 xl:px-2">
      ![favicon](/static/favicons/favicon.ico)
    </div>
  </div>
```

- 对话框

  {' '}

  <iframe
    title="agent"
    src="https://udify.app/chat/oLa1ktkKaO6Syqu9"
    height="500px"
    width="100%"
    className="iframe"
  ></iframe>

```html:agent.html

{' '}

<iframe
  title="agent"
  src="https://udify.app/chat/"
  height="500px"
  width="100%"
  className="iframe"
></iframe>
```

- 本地视频
  {' '}

  <video
    controls
    alt="Video_20240902"
    src="/illustration/2024-001/Video_20240902.mp4"
    width={800}
    height={400}
  />

```html:Video.mp4
<video controls alt="Video" src="/File/Video.mp4" width={800} height={400} />
```

- 在线视频
  <video controls>
    <source
      src="https://github-production-user-asset-6210df.s3.amazonaws.com/28362229/258559849-2124c81f-b99d-4431-839c-347e01a2616c.webm"
      type="video/webm"
    />
  </video>

```html:Video.webm
<video controls>
  <source
    src="https://github-production-user-asset-6210df.s3.amazonaws.com/28362229/258559849-2124c81f-b99d-4431-839c-347e01a2616c.webm"
    type="video/webm"
  />
</video>
```

## Licence

[MIT](https://github.com/timlrx/tailwind-nextjs-starter-blog/blob/main/LICENSE) © [Timothy Lin](https://www.timrlx.com)

```Text:LICENSE
[MIT](https://github.com/timlrx/tailwind-nextjs-starter-blog/blob/main/LICENSE) © [Timothy Lin](https://www.timrlx.com)
```

[^1]: 这是脚注内容。
