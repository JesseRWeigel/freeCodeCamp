---
id: 587d824a67417b2b25124c77
title: Building Locally with react-native init
challengeType: 6
isRequired: false
---

## Description

<section id='description'>
Images 

Now that you've been introduced to JSX syntax and to two fundamental UI elements used in React Native, let's take a look at another element provided by the library.  Like <code>View</code> and <code>Text</code>, the <code>TextInput</code> element is a piece of UI provided by React Native.  You would use it in an app to allow the user to type text into the app on their device's keyboard.  You can think of <code>TextInput</code> in a native app made with React Native the same way you might think of the <code>input</code> element on the web.  Consider the following code:
<blockquote>&lt;View&gt;<br>&nbsp;&nbsp;&lt;TextInput placeholder="Favorite food" /&gt;<br>&lt;/View&gt;</blockquote>
This would render a field that the user could type into presumably to submit their favorite food to the app.
</section>

## Instructions

<section id='instructions'>
Complete the code in the editor so that the user has two fields to type into - one for "Favorite cake" and one for "Favorite dinosaur".  Hint: use the placeholder <code>prop</code> like in the example above to label your input fields.  You will learn more about props in upcoming challenges.
</section>

## Tests

<section id='tests'>

```yml
tests:
  - text: The constant <code>JSX</code> should return a <code>View</code> element.
    testString: assert(JSX.type === 'View', 'The constant <code>JSX</code> should return a <code>View</code> element.');
  - text: There should be two <code>TextInput</code> elements nested inside of the <code>View</code> element.
    testString: assert(Enzyme.shallow(JSX).find('Text').to.have.length(1);, '<code>View</code> should contain a <code>Text</code> element.');
  - text: One <code>TextInput</code> element should include the placeholder text of <code>Favorite cake</code>
    testString: assert(Enzyme.shallow(JSX).contains('Hello World'), 'The <code>Text</code> tag should include the text <code>Hello World</code>');
  - text: One <code>TextInput</code> element should include the placeholder text of <code>Favorite dinosaur</code>
    testString: assert(Enzyme.shallow(JSX).contains('Hello World'), 'The <code>Text</code> tag should include the text <code>Hello World</code>');
```

</section>

## Challenge Seed

<section id='challengeSeed'>

<div id='jsx-seed'>

```jsx
const JSX = (
  <View>
    <Text>Important Questionnaire</Text>
    {/* change code below this line */}

    {/* change code above this line */}
  </View>
);
```

</div>

### After Test

<div id='jsx-teardown'>

```js
AppRegistry.registerComponent('JSX', () => JSX);

AppRegistry.runApplication('JSX', {
  rootTag: document.getElementById('react-root')
});
```

</div>

</section>

## Solution

<section id='solution'>

```js
const JSX = (
  <View>
    <Text>Hello World</Text>
  </View>
);
```

</section>
