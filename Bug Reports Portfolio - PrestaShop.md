# Bug Reports Portfolio – PrestaShop

Below is a curated set of **20 professional bug reports** based on common issues found in the PrestaShop demo store. Each report follows a clean QA standard format so you can directly use them in your GitHub portfolio.

---

## **1. Broken Image on Product Listing Page**

**Module:** Product Catalog
**Severity:** Medium
**Environment:** PrestaShop Demo (Front Office)

**Steps to Reproduce:**

1. Open PrestaShop demo homepage.
2. Scroll to "Popular Products" section.
3. Observe product thumbnails.

**Expected Result:**
All product images should be visible without distortion.

**Actual Result:**
One or more thumbnails appear broken or stretched.

**Attachment:** Screenshot required.

---

## **2. Add to Cart Button Not Responding on First Click**

**Module:** Cart / PDP
**Severity:** High

**Steps:**

1. Navigate to any product.
2. Click "Add to Cart" once.

**Expected:** Cart modal should appear immediately.

**Actual:** No response on the first click; works only after second click.

---

## **3. Search Bar Returns Irrelevant Results**

**Module:** Search
**Severity:** Medium

**Steps:**

1. Type "Shoes" in search bar.
2. Press Enter.

**Expected:** Products related to “Shoes”.

**Actual:** Unrelated products displayed.

---

## **4. Product Price Missing Decimal Formatting**

**Module:** Pricing Display
**Severity:** Low

**Steps:**

1. Browse to "Clothes" category.

**Expected:** Uniform price formatting (e.g., ₹199.00).

**Actual:** Some prices show as "199" without decimals.

---

## **5. Quantity Selector Allows Negative Values**

**Module:** PDP - Quantity Input
**Severity:** High

**Steps:**

1. Open a product page.
2. Click the "-" button repeatedly.

**Expected:** Minimum quantity should be 1.

**Actual:** Goes into negative numbers.

---

## **6. Cart Icon Count Does Not Update Immediately**

**Module:** Header - Cart
**Severity:** Medium

**Steps:**

1. Add an item to cart.
2. Check cart icon quantity.

**Expected:** Count updates instantly.

**Actual:** Count updates only after page refresh.

---

## **7. Checkout Page Loads Slowly (5+ seconds)**

**Module:** Checkout
**Severity:** Performance

**Steps:**

1. Proceed to checkout from cart.

**Expected:** Page should load within 2 seconds.

**Actual:** Takes 5–7 seconds.

---

## **8. Category Filter Not Reset After Navigation**

**Module:** Category Page Filter
**Severity:** Low

**Steps:**

1. Apply filter (size, color).
2. Move to another category.
3. Return back.

**Expected:** Filters reset.

**Actual:** Old filters still applied.

---

## **9. Wishlist Button Shows No Tooltip or Feedback**

**Module:** Wishlist
**Severity:** Low

**Steps:**

1. Hover over wishlist icon.

**Expected:** Tooltip or hover highlight.

**Actual:** No feedback.

---

## **10. Sorting Option “Price: Low to High” Not Working Correctly**

**Module:** Sorting
**Severity:** Medium

**Steps:**

1. Go to "Clothes" category.
2. Select "Price: Low to High".

**Expected:** Items sorted ascending.

**Actual:** Random sorting.

---

## **11. Product Zoom Feature Partially Functional**

**Module:** PDP Image Zoom
**Severity:** Low

**Steps:**

1. Hover over product image.

**Expected:** Smooth zoom.

**Actual:** Zoom flickers.

---

## **12. Add to Cart Modal Shows Old Product Title**

**Module:** Cart Modal
**Severity:** Medium

**Steps:**

1. Add Product A.
2. Quickly add Product B.

**Expected:** Modal shows correct product title.

**Actual:** Shows Product A title again.

---

## **13. Breadcrumb Navigation Skips One Level**

**Module:** Navigation
**Severity:** Low

**Steps:**

1. Navigate: Home → Clothes → Product.

**Expected:** Breadcrumb: Home / Clothes / Product.

**Actual:** Shows only Home / Product.

---

## **14. Cart Allows Checkout With Zero Quantity**

**Module:** Cart / Checkout
**Severity:** High

**Steps:**

1. Set quantity manually to 0.

**Expected:** System should block checkout.

**Actual:** Allows proceeding.

---

## **15. Coupon Code Field Accepts Invalid Characters**

**Module:** Checkout - Coupon
**Severity:** Low

**Steps:**

1. Enter characters like “@@@@@”.

**Expected:** Validation error.

**Actual:** Field accepts without restriction.

---

## **16. Payment Step Does Not Highlight Current Step**

**Module:** Checkout Navigation
**Severity:** UX Issue

**Steps:**

1. Reach payment step.

**Expected:** Payment step should be highlighted.

**Actual:** No visual indicator.

---

## **17. Missing Confirmation Toast After Removing Item from Cart**

**Module:** Cart Action
**Severity:** Medium

**Steps:**

1. Remove an item from cart.

**Expected:** A toast/message confirming removal.

**Actual:** Silent removal.

---

## **18. UI Overlaps on Mobile View**

**Module:** Responsive UI
**Severity:** High

**Steps:**

1. Open homepage on mobile size.
2. Observe header and search bar.

**Expected:** Proper alignment.

**Actual:** Elements overlap.

---

## **19. No Warning When Logging Out During Checkout**

**Module:** Checkout / Session
**Severity:** Medium

**Steps:**

1. Start checkout.
2. Log out.

**Expected:** Warning before losing progress.

**Actual:** Redirects silently.

---

## **20. "Continue Shopping" Button On Cart Redirects Incorrectly**

**Module:** Cart Page
**Severity:** Medium

**Steps:**

1. Go to Cart.
2. Click "Continue Shopping".

**Expected:** Redirects back to last category visited.

**Actual:** Redirects to homepage.

---

If you want, I can also add:

* A polished README for this portfolio repo
* A severity priority matrix
* Screenshots section placeholders
* A CSV/Excel export version
* Additional bug reports for ParaBank, PHPTravels, PrestaShop Admin, etc.

Just tell me **“next”** or what you'd like to add.
