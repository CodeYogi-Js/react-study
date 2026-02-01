# **REACT-STUDY**

# **React all document are avaliable in react.dev**
## **old way to create a React application**
- npx create-react-app 01basic-react
- npx stand for node package executer means
- npx run package without installing globally.
```run create-react-app ---> direactly```
- package is ready made code (software) written by some else. like calculator/whatsapp/react setup tool.
- All are software → in Node.js world we call them packages.
- so npx runs a package. It means: npx runs a ready-made tool/software
```Globally - avaliable every where in your computer.```

### *What does ```npm run start``` means*?
- if you run react first change react repo then cmd run ```nmp run start```
- it tell npm to run a command named start.
- npm stand for node package manager user to manage and run packages.
- ```run``` means execute a script "npm", please run something.
- ```start``` this is a script name. Defined inside package.json This works because start is a special script.

### *What happens after running it?*
- Starts a development server
- Opens browser automatically
- Runs app on`👉 http://localhost:3000`

## **how to create react projcet in vite**
- run `npm create vite@latest`
- npm stand for node package manager. Comes automatically when you install Node.js
- Used to: install tools & libraries, run commands, create projects
- 🧠 Think of npm as: “a helper that downloads and manages JavaScript tools for me”
- create means create a new project.
- vite is a modern build tool. Used to create fast frontend projects (React, Vue, Vanilla JS, etc.)
- `@latest` means use newest stable verstion of vite.

### **What does ```npm run dev``` means?**
- if you run react first change react repo then cmd run ```nmp install```
- `npm` the tool that manage libraries for your project.
- `install` Download & set up required packages Reads package.json
- `Downloads all dependencies.` Puts them into node_modules folder.
- `npm run dev` node package manager run a script.`run` execute a command witten in package.json
- `dev` script name start development server.

### *What happens after running it?*
- Starts a development server
- Opens browser automatically
- Runs app on`👉 http://localhost:3000`

### **What is react component***
- A React component is a small reusable piece of UI (user interface).
- A React component is a function that returns HTML-like code to show on the screen.

### **component name must uppercase**
- *In React, component names must start with an uppercase letter so React can tell the difference between components and normal HTML tags.*
- Simple reason:
👉 React treats lowercase names as HTML elements and uppercase names as custom components.
```jsx 
<mycomponent />❌
<MyComponent />✅
```

### *Example Component*
```jsx
function Hello() {
  return(
      <h1>Hello World</h1>;
      
      )
}
```
- Hello → component name
- return → what to show
- `<h1>Hello World</h1> → UI`

### **What is Fragment**
- React Fragment is a way to wrap multiple elements together without showing anything extra in the browser.
- In simple words: It groups elements, but doesn’t create a new HTML tag.

### *Example Component*
```jsx
function Hello() {
  return(
       <>
      <h1>Hello</h1>
      <p>Welcome</p>
      </>
      )
}
```