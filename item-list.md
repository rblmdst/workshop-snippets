```html
<h1>Item list</h1>
<!-- ADD ITEM FORM -->
<div class="add-item-block">
  <input type="text">
  <button class="btn-add">Add</button>
</div>
<!-- ITEM LIST -->
<div class="item-list">
  <div class="item">
    One
    <button class="btn-delete">Delete</button>
  </div>
  <div class="item">
    Two
    <button class="btn-delete">Delete</button>
  </div>
</div>
```

```scss
/* Global */
html {
  font-size: 10px;
}

* {
  box-sizing: border-box;
  font-size: 2rem;
}

h1 {
  font-size: 3rem;
  text-align: center;
  color: rgb(70, 70, 70);
}
input {
  padding: 0.5rem 1.2rem;
  border-radius: 0.5rem;
  font-size: 2rem;
  min-width: 400px;
}

button {
  padding: 0.5rem 1.2rem;
  border-radius: 0.5rem;
  color: white;
  font-size: 2rem;
  &:not(:disabled) {
    cursor: pointer;
  }
}



/* add form */
.add-item-block {
  display: flex;
  gap: 0.5rem;
  padding: 2rem;
  justify-content: center;
}

.btn-add {
  background-color: rgb(76, 130, 232);
  border: rgb(76, 130, 232);
  &:hover {
    background-color: rgb(72, 121, 212);
    border: rgb(72, 121, 212);
  }
}

/* item list */
.item-list {
  max-width: 800px;
  padding: 2rem;
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
  margin: 0 auto;

  .item {
    display: flex;
    align-items: center;
    justify-content: space-between;
    border: 1px solid rgb(200, 200, 200);
    padding: 1rem;
    border-radius: 0.5rem;

    &:hover {
      background-color: rgb(251, 251, 251);
    }
  }
}

.btn-delete {
  background-color: rgb(255, 55, 55);
  border: rgb(255, 55, 55);

  &:hover {
    background-color: rgb(219, 46, 46);
    border: rgb(219, 46, 46);
  }
}

```