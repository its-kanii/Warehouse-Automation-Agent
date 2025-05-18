# 📦 Warehouse Automation Agent - UiPath Project (Simulated with Notepad)

This project automates warehouse data entry using UiPath, simulating interaction with a Warehouse Management System using Notepad. It reads product data (Product ID, Quantity, and Location) from an Excel sheet and logs it into a Notepad file.

---

## ✅ Features

* Reads product data from an Excel file
* Extracts Product ID, Quantity, and Location for each row
* Simulates data entry into a Notepad application
* Prepares the workflow for easy transition to a real ERP system later

---

## 📁 Input File Structure (Excel)

The input Excel file should have the following headers:

| Product ID | Quantity | Location |
| ---------- | -------- | -------- |
| P101       | 10       | Chennai  |
| P102       | 15       | Delhi    |

---

## 🛠️ Tools Required

* **UiPath Studio**
* Excel file with warehouse data
* Notepad (used for simulation)

---

## 🔄 Workflow Steps

1. **Use Excel File**

   * Reads the data from your Excel spreadsheet.

2. **For Each Excel Row**

   * Iterates through each row of the Excel file.

3. **Assign Variables**

   * Assign values for each column:

     ```vb
     productId = row("Product ID").ToString.Trim
     quantity = row("Quantity").ToString.Trim
     location = row("Location").ToString.Trim
     ```

4. **Open Notepad**

   * `Use Application/Browser` activity points to Notepad.

5. **Type Into**

   * Inside the Notepad window, logs the formatted string:

     ```
     Product: P101, Quantity: 10, Location: Chennai
     ```

---

## 🧪 How to Run

1. Open UiPath Studio.
2. Open the project or create a new one.
3. Create variables: `productId`, `quantity`, and `location` (all of type String).
4. Point the `Use Excel File` activity to your Excel file.
5. Open Notepad manually and then use "Indicate Application" to select it.
6. Run the workflow.

---

## 🧩 Customization

Once you get access to a real ERP or Warehouse Management System, you can:

* Replace the Notepad section with:

  * `Use Application/Browser` pointing to a browser or desktop app
  * `Click`, `Type Into`, `Set Text`, or `Select Item` activities
* Use selectors and dynamic typing based on extracted variables

---

## 📸 Sample Output in Notepad

```
Product: P101, Quantity: 10, Location: Chennai
Product: P102, Quantity: 15, Location: Delhi
```
