# 🟢 What is Batching in React?

👉 **Batching means React groups multiple state updates together and updates the UI only once.**

Simple:

> Many updates → One re-render

---

# 🧠 Why React Does This?

Because re-rendering is expensive.

Instead of:

* Update
* Re-render
* Update
* Re-render
* Update
* Re-render

React does:

* Update
* Update
* Update
* Re-render once ✅

This is batching.

---

# 🟢 Example (Important)

```jsx
function App() {
  const [count, setCount] = useState(0);

  function handleClick() {
    setCount(count + 1);
    setCount(count + 1);
    setCount(count + 1);
  }

  return (
    <>
      <h1>{count}</h1>
      <button onClick={handleClick}>Click</button>
    </>
  );
}
```

You might think:

0 → 1 → 2 → 3

But actual result:

👉 It becomes **1**

Why?

Because React batches them.

All three use the same old value (0).

---

# 🟢 Correct Way When Updating Multiple Times

Use functional update:

```js
setCount(prev => prev + 1);
setCount(prev => prev + 1);
setCount(prev => prev + 1);
```

Now result:

👉 3 ✅

Because each update uses latest value.

---

# 🧠 Simple Memory Trick

Normal update:

```
setCount(count + 1)
```

Uses old value.

Functional update:

```
setCount(prev => prev + 1)
```

Uses latest value.

---

# 🟢 When Does Batching Happen?

In:

* Event handlers
* React 18 automatic batching (even in promises, timeouts)

React 18 improved batching.

---

# 🎯 Interview Short Answer

> Batching is React’s process of grouping multiple state updates into a single re-render for better performance.

---

