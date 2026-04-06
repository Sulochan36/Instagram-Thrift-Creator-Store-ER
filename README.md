
# 🛍️ Instagram-Thrift-Creator-Store-ER

This project contains the ER diagram for a small Instagram-based business that sells thrifted and handmade fashion items.

## 📌 Overview

The goal of this design is to model a growing business that needs to manage:

* Products (thrift & handmade)
* Inventory (including size/color variations)
* Customer orders
* Payments and shipping

## 🧠 Key Design Decisions

* **Product vs Variant Separation**
  Products store general information (name, category, type), while `product_variant` handles size, color, stock, and price.
  This allows proper handling of multiple variations of the same product.

* **Thrift vs Handmade Handling**
  A `type` field is used to distinguish between thrift and handmade items.
  Thrift items are treated as unique (stock = 1), while handmade items can have multiple units.

* **Order System**

  * A customer can place multiple orders
  * Each order can contain multiple items
  * `order_items` acts as a junction table between orders and product variants

* **Payments & Shipping**
  Payment and shipment details are stored separately to keep the design modular and scalable.

## 🔗 Relationships

* One customer → many orders
* One product → many variants
* One order → many order items
* One variant → many order items
* One order → payment(s)
* One order → shipment

## 🎯 Features Covered

* Supports unique and multi-stock products
* Tracks order history per customer
* Handles product variations (size, color)
* Maintains payment and delivery status

## 📁 Submission

The ER diagram is included as:

* [Image](https://github.com/Sulochan36/Instagram-Thrift-Creator-Store-ER/blob/main/Instagram-Thrift-Creator-Store-ER.png)

---


