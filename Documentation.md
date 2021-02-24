<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/Blinkay-Corp">
    <img src="https://blinkay.app/static/assets/images/logo_blue.svg" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">Blinkay Web Application</h3>

  <p align="center">
    Web based application for Blinkay 
    <br />
    <a href="https://github.com/Blinkay-Corp"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://webapp.blinkay.app/integramobile">View Demo</a>
    ·
    <a href="https://github.com/Blinkay-Corp/Blinkay_Web_Project/issues">Report Bug</a>
    ·
    <a href="https://github.com/Blinkay-Corp/Blinkay_Web_Project/issues">Request Feature</a>
  </p>
</p>



<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary><h2 style="display: inline-block">Table of Contents</h2></summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#project-management">Project Management</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
        <li><a href="#contributing">Contributing</a></li>
      </ul>
    </li>
    <li>
      <a href="#web-services">Web Services</a>
      <ul>
        <li><a href="#login">Login</a></li>
        <li><a href="#new-registration">New Registration</a></li>
          <ul> 
             <li><a href="#constructor">Constructor</a></li>
             <li><a href="#validateform">ValidateForm()</a></li>
             <li><a href="#handleselect">HandleSelect()</a></li>
             <li><a href="#handlechange">HandleChange()</a></li>
             <li><a href="#handlesubmit">HandleSubmit()</a></li>
             <li><a href="#render">Render()</a></li>
          </ul>     
        <li><a href="#home-screen">Home Screen</a></li>
        <li><a href="#middleware-api">Middleware API</a></li>
      </ul>
    </li>
    <li>
      <a href="#style-guide">Style Guide</a>
      <ul>
        <li><a href="#basic-rules">Basic Rules</a></li>
        <li><a href="#class-definition">Class Definition</a></li>
        <li><a href="#naming">Naming</a></li>
        <li><a href="#declaration">Declaration</a></li>
        <li><a href="#alignement">Alignement</a></li>
        <li><a href="#quotes">Quotes</a></li>
        <li><a href="#spacing">Spacing</a></li>
        <li><a href="#props">Props</a></li>
        <li><a href="#parentheses">Parentheses</a></li>
        <li><a href="#tags">Tags</a></li>
        <li><a href="#methods">Methods</a></li>
        <li><a href="#ordering">Ordering</a></li>
      </ul>
    </li>
    <li><a href="#librairies">Librairies</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

Our short-term plan is to bring Webapp.Blinkay  and Blinkay.app features within one interface. After the first successful versions, the goal is to implement new features that was not available to the customer on a single platform. This web based project will ensure Blinkay's availability and accessibility to every end-users. 



### Project Management

|       | SOFTWARE MANAGEMENT TOOL |
| ----------- | ----------- |
| Issues and feature tracker      | Holded       |
| Distributed version control system (DVCS)   | Git        |
| Cloud-based DVCS repository   | GitHub        |
| Document/asset storage   | GoogleSlides, GoogleSheets        |
| Team communication   | Slack, GoogleMeets, WhatsApp        |
| Task management   | Holded       |

<!-- GETTING STARTED -->
## Getting Started
To get a local copy up and running follow these simple steps.

### Prerequisites
Please make sure you have `npm` and `node.js` installed.

You can verify both with this command inside your terminal / IDE terminal

`node -v`

`npm -v`

If not installed, please follow these steps :

First, install Homebrew (good utility tool), then Node.js

`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`

`brew install node`

You can now launch a React build with this command :

`npm install -g create-react-app`


In the project directory, you can run:

 `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

### Installation
ToDo

List of librairies/packages to install inside the project.

1. Install NPM packages
   ```sh
   npm install
   ```

<!-- CONTRIBUTING -->
### Contributing
To start contributing to the project, please follow these steps :

1. Create a directory in your personal environment
2. Git Clone the project (`git clone "https://github.com/Blinkay-Corp/Blinkay_Web_Project"`)
3. Git Pull to update the project (`git pull`)
4. Add Changes (`git add file.ext`)
5. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
6. Push to the Branch (`git push`)

#### Note
You can add global configurations :

`git config -- global user.name ”username”`

`git config -- global user.email ”email@domain.ext”`


<!-- USAGE EXAMPLES -->
## Web Services
Use this space to show useful examples of how a project can be used. Additional screenshots, code examples and demos work well in this space. You may also link to more resources.

### Login
ToDo

### New Registration
ToDo

#### Constructor
ToDo

#### ValidateForm()
ToDo

#### HandleSelect()
ToDo

#### HandleChange()
ToDo

#### HandleSubmit()
ToDo

#### Render()
ToDo

### Home Screen
ToDo

### Middleware API
ToDo



<!-- Styling Guide -->
## Style Guide

### Basic Rules
- Only include one React component per file.
    - However, multiple Stateless, or Pure, Components are allowed per file. (Functions or Constants outside component).
- Always use JSX syntax.
    -Be careful, some HTML elements/attributes differs from JSX or is not supported.
- Do not use `React.createElement` unless you’re initializing the app from a file that is not JSX.

### Class Definition
- If you have internal state and/or refs, prefer class extends React.Component over React.createClass.

```jsx
// bad
const Listing = React.createClass({
  // ...
  render() {
    return <div>{this.state.hello}</div>;
  }
});

// good
class Listing extends React.Component {
  // ...
  render() {
    return <div>{this.state.hello}</div>;
  }
}
```

And if you don’t have state or refs, prefer normal functions (not arrow functions) over classes:

```jsx
// bad
class Listing extends React.Component {
  render() {
    return <div>{this.props.hello}</div>;
  }
}

// bad (relying on function name inference is discouraged)
const Listing = ({ hello }) => (
  <div>{hello}</div>
);

// good
function Listing({ hello }) {
  return <div>{hello}</div>;
}
```

### Naming
- **Extensions:** Use .jsx extension for React components. (Views)
- **Filename:** Use PascalCase for filenames.
- **Reference Naming:** Use PascalCase for React components and camelCase for their instances.

```jsx
// bad -> component not in PascalCase
import reactComponent from './ReactComponent';

// good 
import ReactComponent from './ReactComponent';

// bad -> instance not in camelCase
const ReactComponent = <ReactComponent />;

// good 
const reactComponent = <ReactComponent />;
```

- **Component Naming:** Use the filename as the component name. For example, `ReactComponent.jsx` should have a reference name of `ReactComponent.`
```jsx
// bad -> Different names
import Footer from './Footer/index';

// good
import Footer from './Footer';
```

- **Props Naming:** Avoid using DOM component prop names for different purposes.
>Why? People expect props like `style` and `className` to mean one specific thing. In this case, JSX elements. This  makes the code less readable and less maintainable, and may cause bugs.
```jsx
// bad
<MyComponent style="fancy" />

// bad
<MyComponent className="fancy" />

// good
<MyComponent variant="fancy" />
```
### Declaration
- Do not use `displayName` for naming components. Instead, name the component by reference. (See Naming section)
```jsx
// bad
export default React.createClass({
  displayName: 'ReservationCard',
  // stuff goes here
});

// good
export default class ReservationCard extends React.Component {
}
```
### Alignement
- Follow these alignment styles for JSX syntax. 

> Note these alignements should be automatically done when using `tab` or `enter` for indentation.
```jsx
// bad
<Foo superLongParam="bar"
     anotherSuperLongParam="baz" />

// good
<Foo
  superLongParam="bar"
  anotherSuperLongParam="baz"
/>

// if props fit in one line then keep it on the same line
<Foo bar="bar" />

// children get indented normally
<Foo
  superLongParam="bar"
  anotherSuperLongParam="baz"
>
  <Quux />
</Foo>

// bad
{showButton &&
  <Button />
}

// bad
{
  showButton &&
    <Button />
}

// good
{showButton && (
  <Button />
)}

// good
{showButton && <Button />}

// good
{someReallyLongConditional
  && anotherLongConditional
  && (
    <Foo
      superLongParam="bar"
      anotherSuperLongParam="baz"
    />
  )
}

// good
{someConditional ? (
  <Foo />
) : (
  <Foo
    superLongParam="bar"
    anotherSuperLongParam="baz"
  />
)}
```

### Quotes
- Always use double quotes (") for JSX attributes, but single quotes (') for all other JS.

> Why? Regular HTML attributes also typically use double quotes instead of single, so JSX attributes mirror this convention.
```jsx
// bad
<Foo bar='bar' />

// good
<Foo bar="bar" />

// bad
<Foo style={{ left: "20px" }} />

// good
<Foo style={{ left: '20px' }} />
```

### Spacing
- Always include a single space in your self-closing tag.
```jsx
// bad
<Foo/>

// very bad
<Foo                 />

// bad
<Foo
 />

// good
<Foo />
```

- Do not pad JSX curly braces with spaces.
```jsx
// bad
<Foo bar={ baz } />

// good
<Foo bar={baz} />
```

### Props
- Always use camelCase for prop names, or PascalCase if the prop value is a React component.
```jsx
// bad
<Foo
  UserName="hello"
  phone_number={12345678}
/>

// good
<Foo
  userName="hello"
  phoneNumber={12345678}
  Component={SomeComponent}
/>
```
- Omit the value of the prop when it is explicitly true.
```jsx
// bad
<Foo
  hidden={true}
/>

// good
<Foo
  hidden
/>

// good
<Foo hidden />
```

- Always include an alt prop on <img> tags. If the image is presentational, alt can be an empty string or the <img> must have role="presentation".
```jsx
// bad
<img src="hello.jpg" />

// good
<img src="hello.jpg" alt="Me waving hello" />

// good
<img src="hello.jpg" alt="" />

// good
<img src="hello.jpg" role="presentation" />
```

### Parentheses
- Wrap JSX tags in parentheses when they span more than one line.
```jsx
// bad
render() {
  return <MyComponent variant="long body" foo="bar">
           <MyChild />
         </MyComponent>;
}

// good
render() {
  return (
    <MyComponent variant="long body" foo="bar">
      <MyChild />
    </MyComponent>
  );
}

// good, when single line
render() {
  const body = <div>hello</div>;
  return <MyComponent>{body}</MyComponent>;
}
```

### Tags
- Always self-close tags that have no children.
```jsx
// bad
<Foo variant="stuff"></Foo>

// good
<Foo variant="stuff" />
```
- If your component has multiline properties, close its tag on a new line.
```jsx
// bad
<Foo
  bar="bar"
  baz="baz" />

// good
<Foo
  bar="bar"
  baz="baz"
/>
```

### Methods

- Use arrow functions to close over local variables. It is handy when you need to pass additional data to an event handler.
```jsx
function ItemList(props) {
  return (
    <ul>
      {props.items.map((item, index) => (
        <Item
          key={item.key}
          onClick={(event) => { doSomethingWith(event, item.name, index); }}
        />
      ))}
    </ul>
  );
}
```

- Bind event handlers for the render method in the constructor. 
> Why? A bind call in the render path creates a brand new function on every single render.
```jsx
// bad
class extends React.Component {
  onClickDiv() {
    // do stuff
  }

  render() {
    return <div onClick={this.onClickDiv.bind(this)} />;
  }
}

// very bad
class extends React.Component {
  onClickDiv = () => {
    // do stuff
  }

  render() {
    return <div onClick={this.onClickDiv} />
  }
}

// good
class extends React.Component {
  constructor(props) {
    super(props);

    this.onClickDiv = this.onClickDiv.bind(this);
  }

  onClickDiv() {
    // do stuff
  }

  render() {
    return <div onClick={this.onClickDiv} />;
  }
}
```
- Do not use underscore prefix for internal methods of a React component.
> Why? Underscore prefixes are sometimes used as a convention in other languages to denote privacy. But, unlike those languages, there is no native support for privacy in JavaScript, everything is public. 
```jsx
// bad
React.createClass({
  _onClickSubmit() {
    // do stuff
  },

  // other stuff
});

// good
class extends React.Component {
  onClickSubmit() {
    // do stuff
  }

  // other stuff
}
```
- Be sure to return a value in your render methods.
```jsx
// bad
render() {
  (<div />);
}

// good
render() {
  return (<div />);
}
```

### Ordering
- Ordering for `class extends React.Component`:

1. optional `static` methods
2. `constructor`
3. `getChildContext`
4. `componentWillMount`
5. `componentDidMount`
6. `componentWillReceiveProps`
7. `shouldComponentUpdate`
8. `componentWillUpdate`
9. `componentDidUpdate`
10. `componentWillUnmount`
11. event handlers starting with 'handle' like `handleSubmit()` or `handleChangeDescription()`
12. event handlers starting with 'on' like `onClickSubmit()` or `onChangeDescription()`
13. getter methods for `render` like `getSelectReason()` or `getFooterContent()`
14. optional `render` methods like `renderNavigation()` or `renderProfilePicture()`
15. `render`

<!-- LIBRAIRIES -->
## Librairies


<!-- ROADMAP -->
## Roadmap
See the [open issues](https://github.com/Blinkay-Corp/Blinkay_Web_Project/issues) for a list of proposed features (and known issues).

or 

On [Holded](https://app.holded.com/projects/tasks) for a list of personnal tasks.


<!-- CONTACT -->
## Contact
Yan-Alexandre Leclerc - [@GitHub](https://github.com/yanleclerc) - yleclerc@integraparking.com
