---
id: 587d824a67417b2b25124c71
title: Images
challengeType: 6
isRequired: false
---

## Description

<section id='description'>
There are several different ways to include images in your React Native applications. If you have the image locally, you can <code>require</code> it:

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

Notice that in the above examples some of them have height and width style definitions. This is necessary for any images that are not stored locally. Anytime an image isn't displaying on the screen, remember to check if it has height and width styles defined.
</section>

## Instructions

<section id='instructions'>
Add this image from the web inside of the <code>View</code> tag: <a href="https://en.wikipedia.org/wiki/Cat#/media/File:Felis_catus-cat_on_snow.jpg">https://en.wikipedia.org/wiki/Cat#/media/File:Felis_catus-cat_on_snow.jpg</a>
</section>

## Tests

<section id='tests'>

```yml
tests:
  - text: The constant <code>JSX</code> should return a <code>View</code> element.
    testString: assert(JSX.type === 'View', 'The constant <code>JSX</code> should return a <code>View</code> element.');
  - text: There should be one <code>Image</code> element nested inside of the <code>View</code> element.
    testString: assert(Enzyme.shallow(JSX).find('Image').to.have.length(1);, '<code>View</code> should contain a <code>Image</code> element.');
```

</section>

## Challenge Seed

<section id='challengeSeed'>

<div id='jsx-seed'>

```jsx
const JSX = (
  <View>
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
    <Image
      source={{uri: 'https://en.wikipedia.org/wiki/Cat#/media/File:Felis_catus-cat_on_snow.jpg'}}
      style={{width: 100, height: 100}}
    />
  </View>
);
```

</section>
