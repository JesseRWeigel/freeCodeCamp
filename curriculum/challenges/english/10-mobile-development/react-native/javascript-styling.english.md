---
id: 587d824a67417b2b25124c63
title: JavaScript Styling
challengeType: 6
isRequired: false
---

## Description
<section id='description'>
<strong>Intro:</strong> 
TODO: style borders for inputs and more intracate details on styling inputs and buttons



React Native uses JavaScript syntax that is borrowed from CSS for styling components. In React.js for the web, you have the option to use CSS or JS styling; in React Native JS styling is the only option.

How does it work?

Any font styles are applied to the <code>Text</code> tag directly with a style attribute.

```jsx
<Text style={{ fontSize: 24 }}>
```

<b>Note:</b> All of the sizes here (like <code>height</code> and <code>fontSize</code>) are in density independent pixels, which don't have a label like <code>px</code>. React Native uses this system so they will render proportional to any device size.

Likewise, container styles can be applied to <code>View</code> tags.

```jsx
<View style={{ height: 200 }}>
```

Images, as we saw in the last lesson, also can use style definitions.

```jsx
<Image style={{ width: 100, height: 100 }}>
```

You can also pass an object to the style attribute using the recommended <code>StyleSheet</code> function from React Native.

```jsx
const styles = StyleSheet.create({
  container: {
    height: 200
  },
  headerText: {
    fontSize: 24
  },
  image: {
    width: 100,
    height: 100
  }
});
<View style={styles.container}>
  <Text style={styles.headerText}>
  <Image style={styles.image}>
</View>
```

One thing to note is that styles only affect the tag that you attach them to. In other words, if you have tags nested in tags, you still have to apply the styles to every one.

<a href="https://facebook.github.io/react-native/docs/style.html" alt="React Native Styling Documentation" target="_blank">Here is more information about React Native styling.</a>

</section>

## Instructions
<section id='instructions'>
<strong>Instructions:</strong> Create a style object variable called <code>styles</code> using <code>StyleSheet.create</code> and add the keys, <code>headerText</code> and <code>container</code>. Give the container a height of 200 and the headerText a fontWeight of 700. Now attach the styles to the tags using the <code>style</code> attribute on each tag.
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
import { View, Text, StyleSheet } from 'react-native';

const styles = StyleSheet.create({
  container: {
    height: 200
  },
  headerText: {
    fontWeight: 700
  }
});

const JSX = (
  <View style={styles.container}>
    <Text style={styles.headerText}>Welcome to my app</Text>
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
import React from 'react';
import { View, Text, StyleSheet } from 'react-native';

const JSX = (
  <View>
    <Text>Welcome to my app</Text>
  </View>
);
```

</section>
