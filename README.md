# reactfabric

> support fabricjs from react

[![NPM](https://img.shields.io/npm/v/fabricjs-react.svg)](https://www.npmjs.com/package/fabricjs-react) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

## Install

We'll need to install `fabric`, `react` and `react-dom` because are peer dependencies of this library if you haven't yet otherwise install only what you don't have:
```bash
npm install fabricforreact
```

## Usage

```tsx
import React from 'react'

import { FabricJSCanvas, useFabricJSEditor } from 'fabricforreact'

const App = () => {
  const { editor, onReady } = useFabricJSEditor()
  const onAddCircle = () => {
    editor?.addCircle()
  }
  const onAddRectangle = () => {
    editor?.addRectangle()
  }

  return (<div>
    <button onClick={onAddCircle}>Add circle</button>
    <button onClick={onAddRectangle}>Add Rectangle</button>
    <FabricJSCanvas className="sample-canvas" onReady={onReady} />
  </div>)
}

export default App
```
## Methods
```
addCircle() -> To add a circle
addRectangle() -> To add rectangle
addLine() -> To add new line
addImage() -> To add new Image
addText() -> To add new text
deSelectAll() -> To DeSelectAll Element
deleteAll() -> To Delete All Elements
deleteSelected() -> To Delete Selected Elements
setFillColor() -> To fill colors on shapes
setStrokeColor() -> To set colors on stroke
zoomIn() -> To zoom selected elements from canvas
zoonOut() -> To zoom out selected element from canvas
```

## Alternative use cases

### Add image ([#3](https://github.com/asotog/fabricjs-react/issues/3))
For this case, you have to reference the FabricJS dependency to first load the image:

Feel free to collaborate.