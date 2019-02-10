---
id: 587d824a67417b2b25124c79
title: JavaScript Styling - Forms
challengeType: 6
isRequired: false
---

## Description
<section id='description'>
<strong>Intro:</strong> React Native uses JavaScript syntax that is borrowed from CSS for styling components. In React.js for the web, you have the option to use CSS or JS styling; in React Native JS styling is the only option.

How does it work?


```jsx
<Image source={require('./cat.png')} />
```

If it's from the web, you can use it by defining a URI:

```jsx
<Image
  source={{uri: 'https://example.com/cat.png'}}
  style={{width: 100, height: 100}}
/>
```

And if it's encoded image data (e.g. something that starts with <code>data:image/png;base64</code>),

```jsx
<Image
  source={{uri: 'data:image/png;base64,...'}}
   style={{width: 100, height: 100}}
/>
```
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
import React from 'react';
import {
  View,
  Text,
  TextInput,
  Button,
  Stylesheet
} from 'react-native';

const JSX = (
  <View>
    <Text>Welcome to my app</Text>
  </View>
);
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
