Entities
---------
Customer
Order
Order Item
Payment
Menu Item
Menu Category
Location
Employee
Franchise
Inventory
Supplier
Menu Item Ingredient


Logical Relationships
--------------------
---------------------

Customer and Orders
--------------------
Customer places Order

Order Structure
-----------------
Order contains Order Item

Menu Relationships
-------------------
Order Item references Menu Item
Menu Item belongs to Menu Category

Payment
-------
Order is paid through Payment

Location Relationships
----------------------

Location receives Order
Location employs Employee
Location maintains Inventory

Franchise
---------

Franchise owns Location

Inventory and Suppliers
-----------------------

Inventory is supplied by Supplier

Menu Ingredients
----------------

Menu Item uses ingredients from Inventory

Logical Diagram Representation
------------------------------

Customer
   |
   | places
   v
Order
   |
   | contains
   v
Order Item
   |
   | references
   v
Menu Item
   |
   | belongs to
   v
Menu Category


Order
   |
   | paid by
   v
Payment


Location
   | receives
   v
Order


Location
   | employs
   v
Employee


Location
   | maintains
   v
Inventory
   |
   | supplied by
   v
Supplier


Menu Item
   |
   | uses
   v
Inventory


Franchise
   |
   | owns
   v
Location



The logical data model represents the high-level business entities involved in the restaurant system and their relationships. Customers place orders at specific locations. Orders contain multiple order items, each referencing menu items categorized under menu categories. Orders are associated with payments. Locations employ staff and maintain inventory for ingredients. Suppliers provide ingredients for inventory, and menu items use those ingredients. Franchise owners manage restaurant locations, enabling support for both franchise restaurants and food truck operations.