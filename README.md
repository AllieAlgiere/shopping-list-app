# Vue.js 3 Shopping List Application

This is a **Vue.js 3 shopping list app** built using the **Options API**.  
It replicates the functionality demonstrated in the VueSchool “Vue.js 3 Fundamentals” tutorial.

The application allows users to add items to a shopping list, mark them as purchased, flag high-priority items, and manage the list dynamically.

---

## Live Demo

[GitHub Pages Link](https://<yourusername>.github.io)

---

## Features

- **Add Item Button**: Initially displayed; clicking reveals the input area, high-priority checkbox, and Save/Cancel buttons.
- **Input and High Priority Checkbox**: Persist on screen after the first item is added.
- **Save Item**: Adds an item to the list; works via button click or pressing Enter.
- **Cancel Button**: Prompts a confirmation popup; if confirmed, clears all items and hides input row.
- **High-Priority Items**: Displayed in **orange**; purchased items override with grey strike-through.
- **Purchased Items**: Clicking a list item toggles purchased state (grey strike-through).
- **Dynamic List Rendering**: Newest items appear at the top of the list.
- **Success Message**: "Nice job! You've bought all your items!" appears only when all items are purchased.
- **Responsive UI**: Buttons aligned to the right of input for a clean layout.

---

## Rubric Alignment

| Rubric Point | Implementation |
|--------------|----------------|
| **HTML code format** | Semantic HTML using `<h2>`, `<ul>`, `<li>`, `<p>`, `<input>`, `<button>` |
| **Vue template syntax** | `v-if`, `v-for`, `v-model`, `:class`, `@click`, `@keyup.enter` |
| **List rendering** | `v-for="item in reversedItems"` dynamically renders items |
| **User inputs** | Text input (`v-model="newItem"`), checkbox (`v-model="highPriority"`) |
| **User events** | Save, Cancel, Enter key, toggle purchased (`@click`) |
| **Methods** | `saveItem()`, `cancelEdit()`, `togglePurchased(item)`, `showForm()` |
| **Conditional rendering** | `v-if` for Add button, input row, and success message |
| **HTML attribute binding** | `:key="item.id"`, `:class="{ strikeout: item.purchased, priority: item.highPriority && !item.purchased }"` |
| **Dynamic CSS classes** | Applied `strikeout` and `priority` based on item state |
| **Computed properties** | `reversedItems()` (newest items first), `allPurchased()` (success message) |
| **Cancel confirmation + list clearing** | `window.confirm` popup; clears list if confirmed |

---

## Technologies

- **Vue.js 3** (Options API)  
- **HTML5 & CSS3**  
- **GitHub Pages** for hosting  

---

## Usage Instructions

1. Click **Add Item** to show input.
2. Type the item name.
3. Optional: Check **High Priority** for important items.
4. Press **Enter** or click **Save Item** to add.
5. Click a list item to mark it purchased.
6. Click **Cancel** to clear all items (confirmation required).
