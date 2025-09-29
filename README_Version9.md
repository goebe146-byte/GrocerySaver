# GrocerySaver

## Description
GrocerySaver is an app designed for grocery shoppers who want to find the lowest prices at local stores. It helps you compare prices across all nearby grocery stores, making it easy for frugal shoppers to save money on their everyday purchases.

## Features
- **Add Your Local Stores:** Customize the app by adding your favorite or nearby grocery stores.
- **Price Check Items:** Instantly see which store has the lowest price for any grocery item.
- **Shopping List:** Create and manage your own shopping list to stay organized and on budget.

## Team Members
- **Kellan Ruch** – Student / Leader

## Installation / Usage

### Desktop (PC)
Run the application through Java.

### Web App
Open `index.html` in your browser.

### Mobile App
- **Android:** Open and run the project in Android Studio.
- **iOS:** Open and run the project in Xcode.

---

## Class Diagram

```text
+-------------------+
| GrocerySaverApp   |
+-------------------+
| - stores: List<Store> |
| - users: List<User>   |
+-------------------+
| + searchItemByStore(itemName, store) |
| + searchItemCheapest(itemName)       |
| + addStore(store)                    |
| + addUser(user)                      |
+-------------------+

         1
         |
         | *
+-------------------+
| Store             |
+-------------------+
| - name: String    |
| - location: String|
| - inventory: List<Item> |
+-------------------+
| + addItem(item)   |
| + getItem(itemName)|
+-------------------+
         1
         |
         | *
+-------------------+
| Item              |
+-------------------+
| - name: String    |
| - price: Double   |
| - store: Store    |
+-------------------+
| + updatePrice(newPrice) |
+-------------------+

         1
         |
         | *
+-------------------+
| User              |
+-------------------+
| - username: String|
| - email: String   |
| - savedItems: List<Item> |
+-------------------+
| + saveItem(item)  |
| + removeSavedItem(item) |
+-------------------+
```

### Class Descriptions

- **GrocerySaverApp:**  
  The main application class that manages stores and users. It provides methods to search for items by store or find the cheapest item, as well as add new stores and users.

- **Store:**  
  Represents a grocery store, including its name, location, and inventory (a list of items). Methods allow for adding new items and retrieving items by name.

- **Item:**  
  Represents a grocery item with a name, price, and a reference to its store. The price can be updated as needed.

- **User:**  
  Represents a user with a username, email, and a list of saved items. Users can save or remove items from their personal list.

---

## Sample App UI Mockups

### Main Screen

```text
+------------------------------------------------+
|                GrocerySaver Logo               |
+------------------------------------------------+
| [Search by Item]   [Search by Store]           |
|------------------------------------------------|
| Featured Deals:                                |
| - Item 1 - Store Name - $Price                 |
| - Item 2 - Store Name - $Price                 |
| - Item 3 - Store Name - $Price                 |
|------------------------------------------------|
| Navigation: [Home] [Saved Items] [Profile]     |
+------------------------------------------------+
```
*Main screen with quick search, featured deals, and navigation.*

---

### Search Results

```text
+------------------------------------------------+
| Search Item: [__________]  [Search Button]     |
+------------------------------------------------+
| Results:                                       |
| 1. Item Name - Store Name - $Price   [Save]    |
| 2. Item Name - Store Name - $Price   [Save]    |
| 3. Item Name - Store Name - $Price   [Save]    |
|------------------------------------------------|
| Sort by: [Price Low→High] [Store]              |
| Navigation: [Home] [Saved Items] [Profile]     |
+------------------------------------------------+
```
*Search results screen with sort options and save buttons.*

---

### Store Inventory

```text
+------------------------------------------------+
| Select Store: [Dropdown Menu]                  |
+------------------------------------------------+
| Inventory:                                     |
| 1. Item Name - $Price         [Save]           |
| 2. Item Name - $Price         [Save]           |
| 3. Item Name - $Price         [Save]           |
|------------------------------------------------|
| Sort by: [Price Low→High]                      |
| Navigation: [Home] [Saved Items] [Profile]     |
+------------------------------------------------+
```
*Store inventory view with sorting and saving options.*

---

Feel free to update this README to keep it in sync with your app’s growth!