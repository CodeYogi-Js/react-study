# ✅ If interviewer asks: “What is State in React?”
> State is data that a component manages internally and can change over time.
> When state changes, React automatically re-renders the component to update the UI.

If they say “simple explanation”:

> State is changing data that updates the screen.

---

# ✅ “What is a Hook?”
> Hooks are special functions in React that allow functional components to use features like state, lifecycle methods, and other React capabilities.

If they want simple answer:

> A Hook is a special function that lets us use React features inside functional components.

---

# ✅“What is useState?”
> useState is a React Hook that allows us to create and manage state inside a functional component.

---

# 💡 If they ask difference between Hook and State
> State is the data.
> Hook is the function used to create or manage that data.


---


# First: What is State?

👉 **State = changing data that React remembers**

That’s it.

---

### Example

If your screen shows:

```
Count: 0
```

That `0` is state.

When you click button → it becomes:

```
Count: 1
```

React remembered the new value.

So:

> State = value that can change and updates the screen.

---

# Now: What is a Hook?

👉 **Hook = a special React function that gives extra power to a component**

That’s it.

Hooks let you:

* Use state
* Run side effects
* Access DOM
* Manage data

---

# Simple Meaning

* State = memory
* Hook = tool to use that memory


# Example

```js
import { useState } from "react";

function Counter() {
  const [count, setCount] = useState(0);

  return (
    <>
      <h1>{count}</h1>
      <button onClick={() => setCount(count + 1)}>
        Increase
      </button>
    </>
  );
}
```

---

### What is happening?

* `useState` → is a Hook
* It creates state
* `count` → is the state value
* `setCount` → changes the state

---
