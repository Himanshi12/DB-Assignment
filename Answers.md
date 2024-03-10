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
