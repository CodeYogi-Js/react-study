# 🟢 1️⃣ What Are Props?

👉 **Props (short for Properties) are data passed from a parent component to a child component.**

Simple meaning:

> Props = information sent to a component.

---

# 🧠 Think Like This

Component = function
Props = function arguments

Example in normal JavaScript:

```js
function greet(name) {
  return "Hello " + name;
}

greet("Babu");
```

Here:

* `"Babu"` is argument

React version:

```jsx
function Greet(props) {
  return <h1>Hello {props.name}</h1>;
}

<Greet name="Babu" />
```

Here:

* `name="Babu"` is prop

Same idea.

---

# 🟢 2️⃣ Why We Need Props?

Because components should be:

* Reusable
* Dynamic
* Flexible

Instead of hardcoding:

```jsx
<h1>Hello Babu</h1>
```

We use props:

```jsx
<Greet name="Arindam" />
<Greet name="Rahul" />
<Greet name="Sita" />
```

One component → many different outputs.

---

# 🟢 3️⃣ How Props Work (Step-by-Step)

### Parent sends data

```jsx
function App() {
  return <User name="Babu" age={21} />;
}
```

### Child receives data

```jsx
function User(props) {
  return (
    <h1>
      Name: {props.name}, Age: {props.age}
    </h1>
  );
}
```

Output:

```
Name: Babu, Age: 21
```

---

# 🟢 4️⃣ Props Are Read-Only ⚠️

Child cannot change props.

❌ Wrong:

```js
props.name = "Rahul";
```

Props are immutable.

If data needs to change → use **state**.

---

# 🟢 5️⃣ Props Destructuring (Cleaner Way)

Instead of:

```js
function User(props) {
  return <h1>{props.name}</h1>;
}
```

We write:

```js
function User({ name }) {
  return <h1>{name}</h1>;
}
```

Cleaner and professional.

---

# 🟢 6️⃣ Passing Different Types of Props

### String

```jsx
<User name="Babu" />
```

### Number

```jsx
<User age={21} />
```

### Boolean

```jsx
<User isLoggedIn={true} />
```

### Array

```jsx
<User hobbies={["coding", "music"]} />
```

### Object

```jsx
<User info={{ city: "Delhi", country: "India" }} />
```

### Function (Very Important 🔥)

```jsx
function App() {
  function sayHello() {
    alert("Hello!");
  }

  return <Button onClick={sayHello} />;
}
```

Child:

```jsx
function Button({ onClick }) {
  return <button onClick={onClick}>Click</button>;
}
```

This is how parent controls child.

---

# 🟢 7️⃣ Props vs State

| Props                  | State                    |
| ---------------------- | ------------------------ |
| Passed from parent     | Created inside component |
| Read-only              | Can change               |
| Used for communication | Used for dynamic updates |

---

# 🟢 8️⃣ Special Prop: children

```jsx
function Card({ children }) {
  return <div>{children}</div>;
}

<Card>
  <h1>Hello</h1>
</Card>
```

Here:

* `<h1>Hello</h1>` is children prop.

---

# 🎯 Interview-Ready Definition

> Props are read-only data passed from parent to child component to make components reusable and dynamic.
