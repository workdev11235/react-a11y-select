# react-a11y-select

[![Travis][build-badge]][build]
[![npm package][npm-badge]][npm]

A customizable select/dropdown react component with a focus on accessibility (a11y) and ease of use for developers. The goal of this project is to make the component as simple to use as its native HTML counterpart, with improved flexibility of HTML formatted options, and accessibility compliance with full keyboard control.

## Live Demo
http://mikedesjardins.net/react-a11y-select/

## Installation
### via npm
```
npm install react-a11y-select
```

## Usage
Here is a very simple example for how to use the component:

    import { Select, Option } from 'react-a11y-select'
    import 'react-a11y-select/styles.css'
    ...

    <Select>
      <Option value="apple">
        <img src="apple.png" role="presentation" />
        Apple
      </Option>
      <Option value="cherry">
         <img src="cherry.png" role="presentation" />
         Cherry
      </Option>
    </Select>


Simple, right? This will render an unordered list styled as a dropdown/select box. Importantly, it will have all of the correct ARIA and role attributes to make it usable by screen readers, and it will respond as expected to keyboard input.

## Props
The following properties are on the `<Select>` component:

* `label` - the ARIA label attribute for the component. Briefly describes the form field for screen readers. Either `label` or `labelledBy` are required.
* `labelledBy` - the ARIA labelledBy attribute for the compoent. Set to the ID of a `<label>` DOM element which briefly describes the form field to screen readers (note: this is likely going to be deprecated soon)
* `placeholderText` - what appears in the dropdown before a value is selected. Defaults to "Please choose..."
* `indicator` - Unicode character that is used for the arrow indicator in the component. Defaults to `&#x25be` which is rendered as &#x25be;
* `initialValue` - The initial value for the dropdown.
* `onChange` - a handler that is called when the select box value changes. Passed the value that was selected.

The following properties are available on the `<Option>` component:

* `value` - The value associated with the Option.

## This is very much a work-in-progress
There's still a lot more to do on this project and most of it is in flux. It needs more tests, more features, more everything. Even when it's finished, it will probably be most valuable as a "demonstration" component to serve as inspiration for your own work. The props and API are subject to change. Here's a list of my TODOs:

* More tests (there basically aren't any right now)
* Use Flow for typechecking
* An `<OptGroup>` element would be nice.
* Need to record a screencast of the screen reader in action.
* Need to look at selecting a letter jumping in the list.
* Add other callbacks?

See this project's Github issues for other stuff.

## Was this project not quite what you were looking for?
Check out David Clark's awesome aria menubutton project: https://github.com/davidtheclark/react-aria-menubutton
It's another implementation of a React dropdown component where web accessibility is a primary goal.

Also take a look at Kent C. Dodd's Downshift project in Paypal's repo: https://github.com/paypal/downshift It's a far more robust and customizable set of tools for building your own accessible select components, and uses the somewhat less common (but far more flexible) solution of requiring developers to implement their own render methods.

I haven't personally used either of the above libraries in a project (yet), but they both look fantastic and might be just what you need!

## License
MIT

[build-badge]: https://img.shields.io/travis/mdesjardins/react-a11y-select/master.png?style=flat-square
[build]: https://travis-ci.org/mdesjardins/react-a11y-select

[npm-badge]: https://img.shields.io/npm/v/react-a11y-select.png?style=flat-square
[npm]: https://www.npmjs.org/package/react-a11y-select

