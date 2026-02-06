## Environment
- **Environment:** Production  
- **Build-Version:** 05/02/2026  
- **Browser:** Chrome Version 144.0.7559.110 (Official Build) (x86_64)  
- **Device:** MacBook Pro 13inch - 2019  
- **OS Version:** Mac OS Sequoia V-15.7.3  
- **ISP:** Act FiberNet (Fast.com speed check: ~170Mbps)

---

## Title
**Incorrect Product Image Displayed on Product Details Page After Selection**

- **Severity:** Medium (Can be High if it impacts purchase decisions)
- **Pre-condition:** User logged in with Existing/Active user credentials.
- **Test Data:** UserName: `problem_user` | PWD: `secret_sauce`

### Steps to Reproduce
1. Navigated to product listing page.
2. Click on any product title or the product image.
3. Observe the product cards displayed in the listing/grid view.

### Expected Result
Product card should display relevent image that accurately represents the product title shown on the card.

### Actual Result
The product listing violates UI/UX consistency standards by displaying a product image that does not correspond to the associated product title.
### Attachment
<img width="1440" height="900" alt="Bug 1" src="https://github.com/user-attachments/assets/4f7ffc85-b91c-426f-ba27-c50adc1c3e8a" />

---

## Title
**Incorrect Item Details Displayed in Product Details View**

- **Severity:** High (Impacts UI/UX consistency and may lead to incorrect purchase decisions)
- **Pre-condition:** User logged in with Existing/Active user credentials.
- **Test Data:** UserName: `problem_user` | PWD: `secret_sauce`

### Steps to Reproduce
1. Navigate to the product listing page.
2. Identify a product by its title in the grid view.
3. Click on the title to open the product details view.
4. Observe the item details displayed on the details page.

### Expected Result
The product details view should display accurate and consistent item information (title, image, description, price) corresponding to the product selected by the user, in line with standard UI/UX expectations.

### Actual Result
The product details view displays incorrect item details that belong to a different product than the one selected, resulting in a UI/UX data inconsistency.

### Attachment
## Product Catalog Title
<img width="1440" height="900" alt="Screenshot 2026-02-05 at 3 00 15 PM" src="https://github.com/user-attachments/assets/9267261a-d62f-4b01-ba6a-148613d55fc4" />

## Product detail page.
<img width="1440" height="900" alt="Screenshot 2026-02-05 at 3 00 22 PM" src="https://github.com/user-attachments/assets/36811c32-9dcf-4625-adc6-45e101936302" />

---

## Title
**First Name Field Clears and Last Name Field Accepts Only One Character on user details fields**

- **Severity:** Medium (Can be High if it blocks checkout or causes data loss)
- **Pre-condition:** User logged in with Existing/Active user credentials and add products to cart.
- **Test Data:** UserName: `problem_user` | PWD: `secret_sauce`

### Steps to Reproduce
1. Navigate to cart page.
2. Click on Checkout button.
3. Enter a valid value in the First Name field.
4. Enter a valid value in the Last Name field.
5. Observe the First Name field and Last name field after entering the last name.

### Expected Result
The value entered in the First Name field should remain intact when the user enters the Last Name and user should be able to add more than 1 character in the Last name field.

### Actual Result
Entering a value in the Last Name field clears the First Name field, and the Last Name input does not allow more than one character to be entered.

### Attachment
https://github.com/user-attachments/assets/08c6dfd3-650a-4a24-a815-6d6bbd809a8f

---

## Title
**Product Price Is Inconsistent Between Grid View and Detail Page**

- **Severity:** High (Price inconsistency can lead to incorrect purchase decisions)
- **Pre-condition:** User logged in with Existing/Active user credentials and add products to cart.
- **Test Data:** UserName: `visual_user` | PWD: `secret_sauce`

### Steps to Reproduce
1. Navigate to the product listing (grid) page.
2. Note the price value displayed for a specific product.
3. Click on the product to open the product detail page.
4. Navigate back to the product grid page or switch between grid and detail views.
5. Observe the price value displayed for the same product.

### Expected Result
The item price should remain consistent and unchanged when navigating between the product grid page and the product detail page.

### Actual Result
The item price value changes unexpectedly when the user switches between the product grid page and the product detail page for the same item.

### Attachment
## Catalog view price
<img width="458" height="236" alt="Screenshot 2026-02-06 at 10 24 58 AM" src="https://github.com/user-attachments/assets/d267c50b-f2f2-46eb-8c8e-95443504a3bd" />
## Product price in detail view.
<img width="959" height="537" alt="Screenshot 2026-02-06 at 10 25 04 AM" src="https://github.com/user-attachments/assets/b1623103-c14a-4593-9f6a-c875d67dc553" />

---

## Title
**“Add to Cart” Button Misaligned for Last Product Item in Product Grid**

- **Severity:** Low (UI consistency issue)
- **Pre-condition:** User logged in with Existing/Active user credentials and add products to cart.
- **Test Data:** UserName: `visual_user` | PWD: `secret_sauce`

### Steps to Reproduce
1. Navigate to the product listing (grid) page.
2. Observe the “Add to cart” button on the last product item (XYZ).
3. Change the filter sorting.
4. Observe the “Add to cart” button on the last product item (ABC).

### Expected Result
The “Add to cart” button for all product items, including the last item, should be aligned consistently with other product cards in the grid.

### Actual Result
The “Add to cart” button for the last product item is misaligned compared to the buttons on other product cards.

### Attachment
## Befffore filter
<img width="1440" height="900" alt="Screenshot 2026-02-06 at 10 19 30 AM" src="https://github.com/user-attachments/assets/014c9f39-1107-489c-bf46-422f26fb1baa" />
## After filter
<img width="1440" height="900" alt="Screenshot 2026-02-06 at 10 20 11 AM" src="https://github.com/user-attachments/assets/ea40057e-6a09-49c5-8a8f-c1ad96225f41" />

---

## Title
**Remove Button Not Responding in Product Grid View**

- **Severity:** Critical (Prevents users from managing cart items)
- **Pre-condition:** User logged in with Existing/Active user credentials and add products to cart.
- **Test Data:** UserName: `error_user` | PWD: `secret_sauce`

### Steps to Reproduce
1. Navigate to the product listing (grid) page.
2. Add one or more items to the cart.  
   The app is not letting me to sort to narrow the issue.
3. Click the Remove button for any item in the grid view.

### Expected Result
Clicking the Remove button should remove the selected item from the cart and update the button state accordingly.

### Actual Result
- The Remove button does not respond when clicked in the product grid view.
- The item remains in the cart, and no visible UI update occurs.
- There is also a **503 API error** in the network and **uncaught error**

## Attachment
<img width="1440" height="900" alt="Screenshot 2026-02-05 at 3 38 17 PM" src="https://github.com/user-attachments/assets/3be2cef6-8f8d-4674-82a8-6d32ca1ed3f2" />
