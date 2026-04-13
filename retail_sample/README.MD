# Retail Sample Dataset

A small, self-contained retail dataset for SQL workshops and analytics demos. It models a simple e-commerce schema with customers, products, orders, and line items.

## Schema

```
CUSTOMER ──< ORDER ──< ORDER_LINE >── PRODUCT
```

| File | Rows | Primary Key | Description |
|---|---|---|---|
| `CUSTOMER.csv` | 15 | `customer_id` | US-based customers, accounts created 2023–2024 |
| `PRODUCT.csv` | 15 | `product_id` | Products across 8 categories with cost and stock data |
| `ORDER.csv` | 25 | `order_id` | Orders placed Jan–Apr 2025 with status and shipping info |
| `ORDER_LINE.csv` | 55 | `order_line_id` | Individual line items linking orders to products |

## Columns

**CUSTOMER**
`customer_id`, `first_name`, `last_name`, `email`, `phone`, `address`, `city`, `state`, `zip_code`, `created_date`

**PRODUCT**
`product_id`, `product_name`, `category`, `unit_price`, `unit_cost`, `sku`, `stock_quantity`
Categories: Electronics, Apparel, Footwear, Home & Kitchen, Home & Office, Sports & Fitness, Accessories, Stationery, Bags

**ORDER**
`order_id`, `customer_id`, `order_date`, `status`, `shipping_address`, `shipping_city`, `shipping_state`, `shipping_zip`, `order_total`
Statuses: `DELIVERED`, `SHIPPED`, `PROCESSING`, `PENDING`, `CANCELLED`

**ORDER_LINE**
`order_line_id`, `order_id`, `product_id`, `quantity`, `unit_price`, `line_total`

## Sample Questions

- Which customers have placed the most orders?
- What is the total revenue and margin by product category?
- Which orders are still in-flight (not delivered or cancelled)?
- What is the average order value per customer?
- Which products are low on stock?
