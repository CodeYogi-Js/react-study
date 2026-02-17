# 📦 What is `package.json`?

👉 `package.json` is the **identity card of your project**

It tells:

* Project name
* Version
* What libraries you use
* How to run the project

---

## 🧠 Simple Meaning

> `package.json` = List of tools your project needs

---

## Example

```json
{
  "name": "my-app",
  "version": "1.0.0",
  "dependencies": {
    "react": "^18.2.0",
    "react-dom": "^18.2.0"
  },
  "scripts": {
    "start": "vite",
    "build": "vite build"
  }
}
```

---

## 🔹 What is "dependencies"?

These are packages your project needs to run.

Example:

* react
* react-dom
* axios
* express

When you run:

```
npm install
```

NPM reads `package.json`
Then installs those dependencies into `node_modules`.

---

# 🔒 What is `package-lock.json`?

👉 `package-lock.json` is the **exact version tracker**

It locks the **exact versions** of all installed packages.

---

## Why is it needed?

Because versions matter.

Example:

In `package.json`:

```json
"react": "^18.2.0"
```

`^` means:

> Install 18.2.0 OR any newer compatible version.

That means:

* Today → 18.2.0
* Tomorrow → maybe 18.3.1

That can sometimes break projects.

---

## So what does `package-lock.json` do?

It says:

> "No. Install EXACTLY this version."

Example:

```
react: 18.2.0
react-dom: 18.2.0
```

So every developer gets the **same version**.

---

