# E-Commerce-System-Analysis-Document--SAD

This repository contains the **functional analysis**, **UML diagrams**, and **high - level technical documentation** for an E-Commerce web application.

The goal of this project is to build the system **incrementally**, using a  
_User Story → Requirements → Flowchart → Sequence Diagram → Implementation_ approach.

This repo **does NOT contain backend or frontend code**.  
It focuses exclusively on documenting how the system should work.

---

## 📌 Project Purpose

> This project is revesion for the system analysis part in a mentorship program.

### This project exists to:

- Break down each user story into **clear technical workflows**.
- Produce **flowcharts, sequence diagrams, pseudocode**.

> It acts as the **source of truth** for:

- System behavior
- Business logic
- Technical flows
- Developer guidelines

---

## Vision

Becoming the leading e-commerce platform the delivers exceptional shopping experience through innovative technology, personalized service and reliable delivery while empowering business with powerful tools for growth.
Providing customers with easy access to quality products while enabling business to efficiently manage their operation and scale their growth.

---

## User Roles

- Visitor
- Registered Customer
- Administrator

---

## Database Schema

![Database Schema](./DB-Schema.png)

## Schema Overview

- **User**: Base entity for all platform users (Admins & Customers).
- **Admin**: Extends User, includes a `Role`. Responsible for product/category management.
- **Customer**: Extends User, places orders.
- **Product**: Stores product info, linked to Category and Admin (creator).
- **Category**: Lookup table for product categories.
- **Order**: Customer orders, containing total amount, date, and status.
- **Order_Details**: Junction table between Orders and Products (Qty + Unit Price).
- **Pending**: Tracks pending items before deletion (Also could be considered denormalized table).
- **Order_History**: **Denormalized table** storing full order summaries with a JSONB field for products.

## Denormalization Note

The `Order_History` table is intentionally **denormalized** to optimize read performance and simplify reporting.  
It stores:

- Customer full name
- Total amount
- Order date
- Products as **JSONB**

This reduces JOIN operations and speeds up historical order retrieval.

---

## Project Structure

The project is structured by **User Stories**, each in its own folder with its own README file.

---

## **Contact**

For questions or feedback:

- GitHub: [@AbdallaSamirKhalifa](https://github.com/AbdallaSamirKhalifa)
- Email: abdallasamirkhalifa@gmail.com
