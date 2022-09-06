# react-native-canvas 🎇

A Canvas component for React Native

```bash
npm install react-native-webview
react-native link react-native-webview
npm install react-native-canvas
```

## Usage

```TSX
import React, { Component } from 'react';
import Canvas from '@eugnehp/react-native-canvas';

class App extends Component {

  handleCanvas = (canvas) => {
    const ctx = canvas.getContext('2d');
    ctx.fillStyle = 'purple';
    ctx.fillRect(0, 0, 100, 100);
  }

  render() {
    return (
      <Canvas ref={this.handleCanvas}/>
    )
  }
}
```

## API

### Canvas

#### Canvas#height

Reflects the height of the canvas in pixels

#### Canvas#width

Reflects the width of the canvas in pixels

#### Canvas#getContext()

Returns a canvas rendering context. Currently only supports 2d context.

#### Canvas#toDataURL()

Returns a `Promise` that resolves to DataURL.

### CanvasRenderingContext2D

Standard CanvasRenderingContext2D. [MDN](https://developer.mozilla.org/en/docs/Web/API/CanvasRenderingContext2D). Only difference is `await` should be used to retrieve values from methods.

```javascript
const ctx = canvas.getContext('2d');
```

## Image

WebView Image constructor. Unlike in the browsers accepts canvas as first argument. [MDN](https://developer.mozilla.org/en-US/docs/Web/API/HTMLImageElement/Image)

```javascript
const image = new Image(canvas, height, width);
```
