---
id: 587d824a67417b2b25124c59
title: Class Components
challengeType: 6
isRequired: false
---

## Description
<section id='description'>
<strong>Intro:</strong> In React Native you can use ES6 class syntax to define components. The classes you create will always extend the <code>Component</code> class from React.

```js
import React, { Component } from 'react';
import { Text, View } from 'react-native';

class MyComponent extends Component {
  myCustomFunction() {
    return "Hello World"
  }

  render() {
    return (
      <View>
        <Text>{ this.myCustomFunction.bind(this) }</Text>
      </View>
    )
  }
}
```

The only required method inside of a class is <code>render</code>, although you can define as many methods as you want (like the <code>myCustomFunction</code> one above).

<b>Note:</b> the <code>.bind(this)</code> syntax is required for things to run properly in React. We will explore alternatives to this later on. 

</section>

## Instructions
<section id='instructions'>
<strong>Instructions:</strong> Create another method inside of the <code>MyComponent</code> class named <code>returnGreeting</code>. Have that function return the word 'Hello World', just like the above example. Then call the <code>returnGreeting</code> function from inside of <code>View</code> and <code>Text</code> tags in the <code>render</code> function.

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
