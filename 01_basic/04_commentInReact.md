# 🟢 What is a Comment?

👉 Comment = text that **browser ignores**

It is only for **developer notes**.

It does NOT show on screen.

---

# 🟡 1️⃣ Comment in JavaScript (inside .js file)

Same like normal JS:

```js
// This is single line comment

/*
  This is
  multi-line comment
*/
```

---

# 🟢 2️⃣ Comment inside JSX (IMPORTANT ⚠️)

JSX is a little different.

You CANNOT use:

```jsx
// ❌ wrong inside JSX
```

Instead, use:

```jsx
{/* This is JSX comment */}
```

---

# 🔥 Example

```jsx
function App() {
  return (
    <div>
      <h1>Hello</h1>

      {/* This is a comment inside JSX */}

      <p>Welcome</p>
    </div>
  );
}
```

This comment will NOT appear on screen.

---

# 🧠 Why curly braces `{}` ?

Because:

* JSX allows JavaScript inside `{ }`
* Comments are JavaScript
* So we wrap them in `{ }`

---

# 🟡 Super Simple Rule

| Where       | How to Comment    |
| ----------- | ----------------- |
| Outside JSX | `//` or `/* */`   |
| Inside JSX  | `{/* comment */}` |

---

# 🧠 Memory Trick

JSX comment = curly + star
`{/* comment */}`

---