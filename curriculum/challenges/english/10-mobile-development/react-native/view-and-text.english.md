---
id: 587d824a67417b2b25124c57
title: View and Text
challengeType: 6
isRequired: false
---

## Description
<section id='description'>
<section id='description'>
In the last challenge, you used <code>View</code> and <code>Text</code> tags to display some basic hello world text. Let's learn a little more about what those tags do.
If you are familiar with HTML, you might know that some tags are used as containers for page elements - for example, <code>div</code> and <code>span</code> - and other tags are used to hold text - for example, <code>p</code> and <code>h1</code>. Instead of regular HTML, React Native's JSX syntax uses <code>View</code> tags for container elements and <code>Text</code> tags for wrapping text.
Some differences are that <code>View</code> tags render to native iOS and Android views and <code>Text</code> tags are used for all types of text including paragraphs and headers. Any size or styling differences in <code>Text</code> elements are done with styling.
Note: for React Native to render properly, all text must be wrapped inside of a <code>Text</code> element and all <code>Text</code> elements must, in turn, be inside of <code>View</code> tags. Also, <code>View</code> tags cannot be inside of <code>Text</code> tags.
Here are some examples:
<b>Valid React Native JSX:</b>
<blockquote>&lt;View&gt;<br>&nbsp;&nbsp;&lt;Text&gt;Paragraph One&lt;/Text&gt;<br>&nbsp;&nbsp;&lt;Text&gt;Paragraph Two&lt;/Text&gt;<br>&nbsp;&nbsp;&lt;Text&gt;Paragraph Three&lt;/Text&gt;<br>&lt;/View&gt;</blockquote>
<b>Invalid - Text tags must be inside of View tags:</b>
<blockquote>&lt;Text&gt;Paragraph One&lt;/Text&gt;<br></blockquote>
<b>Invalid - Text can only be place inside of Text tags:</b>
<blockquote>&lt;View&gt;Paragraph One&lt;/View&gt;<br></blockquote>
</section>

## Instructions
<section id='instructions'>
Define a new constant <code>JSX</code> that renders a <code>div</code> which contains the following elements in order:
An <code>h1</code>, a <code>p</code>, and an unordered list that contains three <code>li</code> items. You can include any text you want within each element.
<strong>Note:</strong>&nbsp;When rendering multiple elements like this, you can wrap them all in parentheses, but it's not strictly required. Also notice this challenge uses a <code>div</code> tag to wrap all the child elements within a single parent element. If you remove the <code>div</code>, the JSX will no longer transpile. Keep this in mind, since it will also apply when you return JSX elements in React components.
</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: The constant <code>JSX</code> should return an <code>h1</code> element.
    testString: assert(JSX.type === 'h1', 'The constant <code>JSX</code> should return an <code>h1</code> element.');
  - text: The <code>h1</code> tag should include the text <code>Hello JSX!</code>
    testString: assert(Enzyme.shallow(JSX).contains('Hello World'), 'The <code>h1</code> tag should include the text <code>Hello JSX!</code>');

```

</section>

## Challenge Seed
<section id='challengeSeed'>

<div id='jsx-seed'>

```jsx

const JSX = <View></View>;

```

</div>


### After Test
<div id='jsx-teardown'>

```js
AppRegistry.registerComponent('JSX', () => JSX);

AppRegistry.runApplication('JSX', { rootTag: document.getElementById('react-root')});
```

</div>

</section>

## Solution
<section id='solution'>


```js
const JSX = <h1>Hello JSX!</h1>;
```

</section>
