---
id: 587d824a67417b2b25124c68
title: ScrollView
challengeType: 6
isRequired: false
---

## Description
<section id='description'>
<strong>Intro:</strong> React Native is a cross-platform JavaScript framework for building mobile applications that can run outside of the browser — most commonly iOS and Android apps.

React Native, like React, uses a syntax extension of JavaScript called JSX that allows you to write HTML directly within JavaScript. This has several benefits. It lets you use the full programmatic power of JavaScript within HTML, and helps to keep your code readable. For the most part, JSX is similar to the HTML that you have already learned, however there are a few key differences. If you have not done the React challenges on freeCodeCamp.org, it is recommended that you do the first few there to get a feel for JSX before working on these React Native challenges.

You will notice that the Syntax for React Native is almost identical to React's: The main difference being that React Native has doesn't use HTML style tags like <code><p></code> and <code><div></code>. Instead, for text and containers, it uses <code><Text></code> and <code><View></code> to render to native Android and iOS application views.

We are using a browser implementation of the React Native library for this course. This allows us to mimic the functionality of React Native without any complicated setup.
</section>

## Instructions
<section id='instructions'>
<strong>Instructions:</strong> Let's start with a hello world example. Inside of the <code>View</code> tag, place a <code>Text</code> tag with the words 'Hello World' inside it.
</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: The constant <code>JSX</code> should return a <code>View</code> element.
    testString: assert(JSX.type === 'View', 'The constant <code>JSX</code> should return a <code>div</code> element.');
  - text: The variable <code>JSX</code> contain a <code>View</code> element.
    testString: assert(Enzyme.shallow(JSX).find('View').to.have.length(1);, '<code>JSX</code> should render an <code>View</code> element.');
  - text: There should be a <code>Text</code> element nested inside of the <code>View</code> element.
    testString: assert(Enzyme.shallow(JSX).find('Text').to.have.length(1);, '<code>View</code> should contain a <code>Text</code> element.');
  - text: The <code>View</code> tag should include the text <code>Hello World</code>
    testString: assert(Enzyme.shallow(JSX).contains('Hello World'), 'The <code>Text</code> tag should include the text <code>Hello World</code>');

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
const JSX = <View><Text>Hello World</Text></View>;
```

</section>
