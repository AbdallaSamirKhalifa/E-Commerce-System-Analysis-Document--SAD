# User Story 009: Password Recovery

**ID:** US-009  
**Role:** Administrator

---

## Description

A brief summary of the user story:

> As an administrator I want to add, edit, and delete products So that I can maintain an up-to-date product catalog.

---

## Acceptance Criteria

Specific conditions that must be met for this user story to be considered complete:

- Admin can create new products with all required fields
- Admin can edit existing product details
- Admin can delete products (soft delete - mark as inactive)
- Product images can be uploaded (max 5MB, JPG/PNG only)
- Stock quantity can be updated
- Changes are reflected immediately on the storefront
- Validation prevents negative prices or stock quantities

---

## Business Roles

- Deleted products are archived, not permanently removed
- Products in pending orders cannot be deleted
- Price changes don't affect existing orders
- Stock updates trigger low-stock alerts if quantity < 10

---

## US-009.1: Create New Product

### Administrator can create new product.

[Create New Product](./Create-New-Product/)

---

## US-009.2: Edit Product

### Administrator can edit product details.

[Update Product](./Edit-Product/)

---

## US-009.3: Delete Product

### Admin can delete products (soft delete - mark as inactive)

[Delete Product](./Delete-Product/)

> Products in pending orders cannot be deleted.
