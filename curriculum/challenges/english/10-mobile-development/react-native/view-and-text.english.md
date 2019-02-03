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
An <code>View</code>, and an unordered list that contains three <code>Text</code> items. You can include any text you want within each element.
</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: The component <code>Example</code> should render an <code>View</code> element.
    testString: assert(Enzyme.shallow(React.createElement(Example)).find('View'), 'The component <code>Example</code> should render an <code>View</code> element.');
  - text: The <code>View</code> tag should include three <code>Text</code> elements.
    testString: assert(Enzyme.shallow(React.createElement(Example)).find('Text').length === 3, 'The <code>View</code> tag should include three <code>Text</code> elements.');

```

</section>

## Challenge Seed
<section id='challengeSeed'>

<div id='jsx-seed'>

```jsx
import React from 'react';
import { View, Text } from 'react-native';

const JSX = (
  <View>
  </View>
);
```

</div>

### Before Test
<div id='jsx-setup'>

```js
window.View = window.ReactNative.View;
window.Text = window.ReactNative.Text;
```

</div>


### After Test
<div id='jsx-teardown'>

```js

class Example extends React.Component {
  render() {
    return JSX;
  }
}

window.ReactNative.AppRegistry.registerComponent('JSX', () => Example);

window.ReactNative.AppRegistry.runApplication('JSX', { rootTag: document.getElementById('root')});
```

</div>

</section>

## Solution
<section id='solution'>


```js
import React from 'react';
import { View, Text } from 'react-native';

const JSX = (
  <View>
    <Text>Hello World</Text>
  </View>
);
```

</section>
