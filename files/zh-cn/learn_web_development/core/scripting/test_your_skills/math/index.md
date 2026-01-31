---
title: "技能测试：数学"
short-title: "测试：数学"
slug: Learn_web_development/Core/Scripting/Test_your_skills/Math
page-type: learn-module-assessment
sidebar: learnsidebar
l10n:
  sourceCommit: 9d3d642daf9df9ece138fa39972edc5f7d6dcd6b
---


{{PreviousMenuNext("Learn_web_development/Core/Scripting/Math", "Learn_web_development/Core/Scripting/Strings", "Learn_web_development/Core/Scripting")}}

本页面的测试旨在帮助你评估自己是否掌握了 [JavaScript 基础数学——数字与运算符](/zh-CN/docs/Learn_web_development/Core/Scripting/Math) 这篇文章的内容。

> [!NOTE]
>  [测试你的技能](/zh-CN/docs/Learn_web_development#test_your_skills) 使用指南。 你也可以通过我们的 [沟通渠道](/zh-CN/docs/MDN/Community/Communication_channels)联系我们。

## 数学 1

让我们先来测试一下你对基本数学运算符的掌握。你会创建四个变量，把其中两个相加，再从另两个数中用一个减去另一个，然后把这两次运算的结果相乘；最后，你再写一个测试来证明得到的值是偶数。

完成本任务要求：

1. 创建四个变量分别存放数字，给变量语义化的命名。
2. 将前两个变量相加，并将结果存入另一个变量。
3. 用第三个变量减去第四个变量，将结果存入另一个变量中。
4. 将第二步和第三步得出的结果相乘，把乘积存入名为`finalResult`的变量中。
5. 使用其中一个[算术运算符](/zh-CN/docs/Learn_web_development/Core/Scripting/Math#arithmetic_operators)检查`finalResult`是否为偶数，将判断结果（偶数为0、奇数为1）存入名为`evenOddResult`的变量中。
   
要通过此测试， `finalResult` 的值应该为 `48` ， `evenOddResult` 的值应为 `0`.

<!-- Code shared across examples -->

```html hidden live-sample___math-1 live-sample___math-2 live-sample___math-3
<section></section>
```

```css hidden live-sample___math-1 live-sample___math-2 live-sample___math-3
* {
  box-sizing: border-box;
}

p {
  color: purple;
  margin: 0.5em 0;
}
```

<!-- Example-specific code -->

```js live-sample___math-1
let finalResult;
let evenOddResult;

// 请勿修改上方代码！

// 在此处添加你的代码

// 请勿修改下方代码！

const section = document.querySelector("section");
const para1 = document.createElement("p");
const finalResultCheck =
  finalResult === 48 ? `是的，做得好！` : `最终结果是48？ ${finalResult}`;
para1.textContent = `Is the finalResult 48? ${finalResultCheck}`;
const para2 = document.createElement("p");
const evenOddResultCheck =
  evenOddResult === 0
    ? "结果为偶数！"
    : "结果为奇数，嗯……";
para2.textContent = evenOddResultCheck;
section.appendChild(para1);
section.appendChild(para2);
```

{{ EmbedLiveSample("math-1", "100%", 80) }}

<details>
<summary>点击此处显示解决方案</summary>

你完成的JavaScript应该看起来像这样：

```js
// ...
// 请勿修改以上代码！

const number1 = 4;
const number2 = 8;
const number3 = 12;
const number4 = 8;

const additionResult = number1 + number2;
const subtractionResult = number3 - number4;

finalResult = additionResult * subtractionResult;

evenOddResult = finalResult % 2;

// 请勿修改以下代码！
// ...
```

</details>

## 数学 2

在第二项任务中，会为你提供两个计算式，其结果分别储存在变量`result`和`result2`中。
你需要将这两个计算结果相乘，并将最终结果格式化为保留两位小数。

完成本任务要求：

1. 将 `result` 和 `result2` 相乘，并将结果重新赋回给`result`（使用赋值简写）。
2. 将 `result` 格式化保留两位小数，并将其存入名为 `finalResult` 的变量中。
3. 使用 `typeof` 检查 `finalResult` 的数据类型，如果是字符串类型，则将其转换为数字类型并将结果储存在一个名为 `finalResult` 的变量中。

要通过本测试，`finalNumber` 的结果需为`4633.33`。你可能需要考虑运算符优先级，为输入表达式添加或修改部分括号以得到正确输出。

```js live-sample___math-2
// 最终结果应为4633.33

let result = 7 + 13 / 9 + 7;
let result2 = (100 / 2) * 6;

// 在此处添加代码

// 请勿修改以下代码！

const section = document.querySelector("section");
const para1 = document.createElement("p");
para1.textContent = `你的最终结果finalResult是 ${finalResult}`;
const para2 = document.createElement("p");
const finalNumberCheck =
  isNaN(finalNumber) === false
    ? "finalNumber是数字类型，做得好！"
    : `哎呀！ finalNumber不是数字类型。`;
para2.textContent = finalNumberCheck;
section.appendChild(para1);
section.appendChild(para2);
```

{{ EmbedLiveSample("math-2", "100%", 80) }}

<details>
<summary>点击此处显示解决方案</summary>

你完成的JavaScript应该看起来像这样：

```js-nolint
// 最终结果应为4633.33

let result = (7 + 13 / 9) + 7;
let result2 = 100 / 2 * 6;

result *= result2;

const finalResult = result.toFixed(2);

const finalNumber = Number(finalResult);

// 不要修改下面的代码！
// ...
```

</details>

## 数学 3

在这篇文章的最后一个任务中，我们希望你编写一些测试代码。

完成本任务要求：

1. 这里有三组内容，每组都包含一个陈述和两个变量。对于每一组，请编写一个测试来验证该陈述是否成立。
2. 将这些测试的结果分别存入名为  `weightComparison` 、 `heightComparison`  和  `pwdMatch`  的变量中。

```js live-sample___math-3
// 陈述1：大象的体重比老鼠轻
const eleWeight = 1000;
const mouseWeight = 2;
// 陈述2：鸵鸟比鸭子高
const ostrichHeight = 2;
const duckHeight = 0.3;
// 陈述3：两个密码一致
const pwd1 = "stromboli";
const pwd2 = "stROmBoLi";

// 请勿修改以上代码！

// 在此处添加你的代码

// 请勿修改以下代码！

const section = document.querySelector("section");
const para1 = document.createElement("p");
const para2 = document.createElement("p");
const para3 = document.createElement("p");
const weightTest = weightComparison
  ? "真 — 大象的体重比老鼠轻！？"
  : "假 — 大象的体重当然比老鼠重！";
const heightTest = heightComparison
  ? "真 — 鸵鸟确实比鸭子高！"
  : "假 — 居然鸭子比鸵鸟还高！？";
const pwdTest = pwdMatch
  ? "真 — 两个密码是匹配的。"
  : "假 — 两个密码不匹配；请检查一下。";
para1.textContent = weightTest;
section.appendChild(para1);
para2.textContent = heightTest;
section.appendChild(para2);
para3.textContent = pwdTest;
section.appendChild(para3);
```

{{ EmbedLiveSample("math-3", "100%", 80) }}

<details>
<summary>点击此处显示解决方案</summary>

你完成的JavaScript应该看起来像这样：

```js-nolint
// ...
// 请勿修改以上代码！

const weightComparison = eleWeight < mouseWeight;
const heightComparison = ostrichHeight > duckHeight;
const pwdMatch = pwd1 === pwd2;

// 请勿修改以下代码！
// ...
```

</details>

{{PreviousMenuNext("Learn_web_development/Core/Scripting/Math", "Learn_web_development/Core/Scripting/Strings", "Learn_web_development/Core/Scripting")}}
