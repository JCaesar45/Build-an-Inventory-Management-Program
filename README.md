````markdown
# Inventory Management Program

This project implements a simple inventory management system using JavaScript. It allows you to add, update, find, and remove products from an inventory array.

## Features

- Store products as objects with `name` (lowercase string) and `quantity` (integer) in an inventory array.
- Find a product's index in the inventory by name (case-insensitive).
- Add new products or update quantities of existing products.
- Remove specified quantities of products, with appropriate handling if quantity is insufficient or product not found.
- Automatically remove products from inventory if quantity reaches zero.

## Functions

### `findProductIndex(productName)`

- **Input:** `productName` (string)
- **Output:** Index (integer) of the product in the inventory array or `-1` if not found.
- **Behavior:** Case-insensitive search using lowercase comparison.

### `addProduct(product)`

- **Input:** `product` (object with `name` and `quantity`)
- **Behavior:**  
  - If the product exists, update its quantity and log:  
    `"<product-name> quantity updated"`
  - If new, add to inventory and log:  
    `"<product-name> added to inventory"`

### `removeProduct(productName, quantity)`

- **Input:** `productName` (string), `quantity` (integer)
- **Behavior:**  
  - If product not found, logs:  
    `"<product-name> not found"`
  - If quantity insufficient, logs:  
    `Not enough <product-name> available, remaining pieces: <current-quantity>`
  - Otherwise, subtracts quantity, logs:  
    `Remaining <product-name> pieces: <updated-quantity>`
  - Removes product from inventory if quantity reaches zero.

## Usage Example

```js
addProduct({ name: "apple", quantity: 10 });  // apple added to inventory
addProduct({ name: "Apple", quantity: 5 });   // apple quantity updated
removeProduct("apple", 8);                     // Remaining apple pieces: 7
removeProduct("banana", 1);                    // banana not found
```

## How to Run

* Include the JavaScript functions in your project.
* Use the functions to manage the `inventory` array as shown in the usage example.
* Logs will be printed to the console according to actions performed.

---

This program is designed for educational purposes and can be extended to include features like persistent storage, user input handling, or integration with a UI.

---

**Author:** Jordan Leturgez
**Date:** 2025-05-23

