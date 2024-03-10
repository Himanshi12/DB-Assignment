1. Explain the relationship between the "Product" and "Product_Category" entities from the above diagram.

In Products table, we have all products data having attributes particular id(unique id assigned to each particular product) Primay_Key,
name(Name of the product),
description(descriptionof the product),
SKU(stock keeping unit is a distinct string of letters and numbers that helps retailers identify every product in their inventory),
category_id(Product category which it belong to),
inventory_id(Inventory category which it belong to),
price(Price of the product),
discount_id(discount_id refer to the id which correspond to particular discount_rate),
created_at(Date at which product is created),
modified_at(Date at which product is modified),
deleted_at(Date at which product is deleted)

In Product_Category table, we have all the caterogies which any product can belong to having attributes
id (id of the caterogy which any product can belong to) Primay_Key,
name (name of the product category),
desc (descriptionof the product category),
created_at(Date at which Product product category is created),
modified_id (Date at which product category is modified),
deleted_id (Date at which product category is deleted)

Products table and Product_Category table, have many to one relationship means
many products can belong to one product category.
category_id in products table is referenced to id in product_category.
Where one product category can have many products associated with it, but each product belongs to only one category.
This is typically represented by a foreign key in the "Product" table that references the primary key of the "Product_Category" table.

2. How could you ensure that each product in the "Product" table has a valid category assigned to it?

We ensure that each product in the "Product" table has a valid category assigned to it as it is referenced to id in "Product_Category" table
which is primay key of the "Product_Category" table which should be valid and unique.

To ensure that each product in the "Product" table has a valid category assigned to it, we can implement referential integrity constraints in your database schema.
Referential integrity constraints enforce relationships between tables by ensuring that values in one table's foreign key columns refer to existing primary key values in another table.
We could achieve this by :
Foreign Key Constraint: In the "Product" table, include a foreign key column that references the primary key of the "Product_Category" table.
This foreign key column should store the category ID for each product.
Primary Key Constraint: In the "Product_Category" table, ensure that the category ID is a primary key, meaning it uniquely identifies each category.
Referential Integrity Constraint: Define a foreign key constraint on the foreign key column in the "Product" table, specifying that it references the primary key column in the "Product_Category" table.
This constraint ensures that each value in the foreign key column of the "Product" table must exist as a primary key value in the "Product_Category" table.

