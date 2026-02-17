# 🟢 What is `ReactDOM.createRoot()` ?

👉 It tells React:

> “This is the place in HTML where you should show my app.”

---

# 🧠 First Understand This

In your **index.html** you have:

```html
<div id="root"></div>
```

This is just an empty box 📦

Nothing is inside it.

---

# 🟢 Now Look at This

```js
const root = ReactDOM.createRoot(document.getElementById("root"));
```

What this means:

1️⃣ Find the box with id `"root"`
2️⃣ Prepare it for React
3️⃣ Make it ready to show the app

---

# 🟢 Then This Line

```js
root.render(<App />);
```

This means:

> “Put my App component inside that box.”

---

# 🎬 Real Life Example

Think like this:

* `index.html` = empty TV screen 📺
* `div id="root"` = screen frame
* `createRoot()` = turn on TV
* `render(<App />)` = show the channel

---

# 🔥 Why do we need `createRoot()`?

Because React 18 introduced a **new rendering system**.

Before React 18, we used:

```js
ReactDOM.render(<App />, document.getElementById("root"));
```

Now we use:

```js
ReactDOM.createRoot(...).render(...)
```

It is:

* Faster
* More powerful
* Supports new React features

---
