## 🌍 Browser Support

| ![Chrome](https://raw.github.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) | ![Edge](https://raw.github.com/alrra/browser-logos/master/src/edge/edge_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.github.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| --- | --- | --- | --- | --- |
| Chrome 39.0+ ✔ | Edge 12.0+ ✔ | Firefox 30.0+ ✔ | IE 11+ ✔ | Safari 9.1+ ✔ |

## 📦 Install

`npm install dynamic-antd-theme` or `yarn add dynamic-antd-theme`


## 🔨 Usage

The best usage of the dynamic-antd-theme is in the common compnent (Layout/Header etc...) of your application.

```
// Layout.js
...
import DynamicAntdTheme from 'dynamic-antd-theme';
...

<div className='theme-container'>
  <span>Change antd theme: </span>
  <DynamicAntdTheme />
</div>

```
### More Example

```

<DynamicAntdTheme primaryColor='#77dd66' />

<DynamicAntdTheme storageName='my-custom-define-color' />

<DynamicAntdTheme style={{ display: 'margin: 10px' }} />

function themeChangeCallback (color) {
  document.getElementById('my-header-bar').style.backgroundColor = color;
}

<DynamicAntdTheme themeChangeCallback={this.themeChangeCallback} />

```

## ✨ Props

| Props       | Type   | Default                  | Description         |
| ---------- | ------ | --------------------- | ------------ |
| primaryColor   | String | #1890d5 |  your antd initial @primary-color      |
| storageName   | String |   custom-antd-primary-color  | the name that is saved in the localStorage    |
| style   | Object |  null  | you can custom the component style simply  |
| placement   | String | bottomRight |  change the color-picker position, `bottom, bottomRight, right, topRight, top, topLeft, left, bottomLeft`|
| themeChangeCallback   | Func | null | you can do something use themeColor when themeColor changed. |

## 🌞 Export
| export       | Description         |
| ---------- | ------------ |
| default  | The <DynamicAntdTheme /> component   |
| generateThemeColor   | `param: color`, generate colorObj based on color  |
| changeAntdTheme   | `param: colorObj`, change the antd theme |

#### Example
```
import { generateThemeColor, changeAntdTheme } from 'dynamic-antd-theme';
...

<Button
  onClick={
    () => {
      const color = 'blue';
      changeAntdTheme(
        generateThemeColor(color);
      );
    }
  }
>Change Theme</Button>
```

## ⚠️ Attention

**This solution is easy to use, so it is prone to problems. We hope you can give us timely feedback. For example, if there is a problem with any component, we will fix the updated version as soon as possible.**

 - The current version requires your antd version to be lower than v3.19.0
   
> The antd version is higher than v3.19.0 you can also use it, if have some problems remember give me an issue. 

 - ...Plugin versions are updated from time to time based on antd (new antd components are updated)

## 🔗 Changelogs

 - v0.1.3
    
    Fix the Slider Component.
 
 - v0.1.4
    
    Fix repeat insert `<style>` tag.
  
 - v0.1.5
  
    Add placement props, `bottom, bottomRight, right, topRight, top, topLeft, left, bottomLeft`. Default is `bottomRight`.
  
 - v0.1.6
  
    Add themeChangeCallback props, you can do something use themeColor when themeColor changed.
  
 - v0.2.0

    Fix ant-design table tr background when cursor hovered.
  
 - v0.2.4

    Support IE 11+.
  
 - v0.2.6
  
    Fix DatePicker current date color.

 - v0.3.0
  
    Export `{ generateThemeColor, changeAntdTheme }` methods to help the developer who don't need react-colorPicker
  
 - v0.3.2
  
    Fix `<Button type='danger' />` bug, when hover the font color is primary-color.
  
 - v0.3.6

    Fix DateRangePicker some bugs.

 - v0.3.7
  
    Fix`table:hover`in antd^3.20.0+

 - v0.3.8

    Fix`calender`some bugs.

 - v0.3.9

    Fix`tree-table-icon`bug.


