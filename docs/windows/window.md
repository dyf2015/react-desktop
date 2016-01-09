# Window Component

<a id="demo-Windows.Window"></a>

## Properties

Property            | Type   | Description
:------------------ | :-----:| :----------
background          | string | Sets the background color of a component.
chrome              | bool   | Sets the chrome of the window.
color               | string | Sets the color of the window and components.
height              | number | Sets the height of a component.
hidden              | bool   | Sets the visibility of a component.
horizontalAlignment | string | Sets the horizontal alignment of the component's content<br/>__Property value__ _"left"_, _"center"_, _"right"_
padding             | string | Sets the padding inside a component.<br/>__E.G.__ _"30px 20px"_
style               | object | Sets the style of the component.
theme               | string | Sets the UI theme that is used by this component and its children elements.<br/>__Property value__ _"light"_, _"dark"_
verticalAlignment   | string | Sets the vertical alignment of the component's content.<br/>__Property value__ _"top"_, _"center"_, _"bottom"_
width               | number | Sets the width of a component.

## Examples

```jsx
import React, { Component } from 'react';
import { Window, TitleBar, Text } from 'react-desktop/windows';

export default class extends Component {
  getDefaultProps() {
    return {
      color: '#cc7f29',
      theme: 'dark'
    };
  }

  render() {
    return (
      <Window
        color={this.props.color}
        theme={this.props.theme}
        chrome
        width="1000px"
        height="600px"
        padding="12px"
      >
        <TitleBar title="My Windows Application" controls/>
        <Text color={this.props.theme === 'dark' ? 'white' : '#333'}>Hello World</Text>
      </Window>
    );
  }
}
```