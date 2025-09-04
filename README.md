# n8n-debug-node

A plug-and-play **DEBUG Code node** for [n8n](https://n8n.io) that shows the **real, runtime item-reference syntax** (`$item(X).json.*`, etc.) for all your workflow data fields—no more relying on sometimes-misleading “green/red” UI highlights.

---

## ✨ Why Use This?

- **Copy exact reference syntax:** Reveals the *real* `$item(...)` field paths you need, as n8n actually resolves them during execution.
- **Save time:** Eliminates trial-and-error when the UI’s “green/red” dot highlights are wrong or ambiguous.
- **Fully standalone:** No changes needed upstream, just plug in and debug.

---

## 🚀 Quick Start

1. Download [`n8n-debug-node.json`](./n8n-debug-node.json) from this repo.
2. Import into your n8n (Workflows > Import > File).
3. Open workflow, copy the DEBUG-node, and paste it into any workflow.
4. Connect DEBUG-node after any node and Execute—you’ll see all available runtime item paths.

---

## 🛠️ What It Outputs

For each incoming item, you get:

```javascript
{
  "DEBUG-INFO-Item-0": {
    "json": [
      "$item(0).json.name",
      "$item(0).json.data.id"
    ],
    "binary": [
      "$item(0).binary.file"
    ],
    "miscellaneous-or-other": [
      "$item(0).pairedItem"
    ]
  }
}
```

Just copy & paste the paths as needed!

---

## 👩‍💻 Use Cases

- **Quickly copy the correct item syntax for the Expression Editor.**
- **Debug how Merge, Split, or other advanced nodes shape your data.**
- **Avoid wasted time and broken workflows due to misleading UI syntax clues.**

---

## FAQ

**Does this modify my data?**  
No, it summarizes paths and passes data through unchanged.

**Can I use it anywhere?**  
Yes—simply paste after any node whose outputs you want to inspect.

---

## License

MIT

---

## Credit

Star or PR welcome if this helped you!
