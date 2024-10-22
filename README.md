# SQL BoxStore
Developed a relational OLAP database for a BoxStore, focusing on data analysis, reporting, and normalization principles. Working with multi-dimensional datasets and complex relationships has given me invaluable insights into creating scalable and efficient databases for business intelligence.

## 💡 Key Learnings & Takeaways
📊 OLAP Database Design: Built the system with an OLAP approach to enable powerful analytical queries. Focused on reporting and aggregation across dimensions like customers, products, and time.

🔄 Data Normalization & Efficiency: Applied 3rd Normal Form (3NF) to reduce redundancy, streamline queries, and improve data integrity.

🔗 Managing Many-to-Many Relationships: Implemented join tables to handle complex relationships between orders, items, and manufacturers.

⚙️ Dynamic Tax Calculations: Created tax calculation views by cross-joining taxes with order dates to ensure accurate rates at the time of purchase.

⚡ Performance Optimization: Balanced query performance with scalability to support large datasets and future data growth. Tuned queries to generate OLAP-style reports across multiple dimensions.

## Tables Created
1. people TABLE (p)
2. geo_address_type TABLE (gat)
3. geo_country TABLE (gco)
4. geo_region TABLE (grg)
5. geo_towncity TABLE (gtc)
6. people_employee TABLE (pe)
7. manugacturer TABLE (m)
8. item_type (it)
9. item (i)
10. item_inventory (ii)
11. item_price (ip)
12. taxes (t)
13. orders (o)
14. orders__item (oi)

## JOINS
1. geo_region to geo_country
2. geo_towncity to geo_region to geo_country
3. item through manufacturer and item_type
4. item through item_inventory
5. orders through people, people_employee
6. orders__item through
   , orders
   , item join through manufacturer and item_type 
   , item_price 
   , item_inventory
   
## VIEWS
1. Boxstore Inc. only information
2. the orders JOIN to employees and customers
3. the orders__item JOIN to display the columns we see on a receipt as line items, still showing serials numbers in the comma delimited list
4. group the previous view by orders, removing all unnecessary columns
5. cross join to the taxes table using the order_date, to get the current taxes and multiply by the subtotal
6. using the previous view, add the subtotalsafter taxes together

## Entity Relationship Diagram (ERD)
![SQL_BoxStore_ERD](https://github.com/user-attachments/assets/7f1f3bd3-b0e1-476b-bedf-f2fefbf05138)

## Few Snapshots of the Code 
![SQL_1](https://github.com/user-attachments/assets/8fb1dbb8-a559-4748-8038-fb6941fef85b)
![SQL_2](https://github.com/user-attachments/assets/532b743d-2624-4ded-83e9-5492c0f9a67f)

## Data Normalization
![SQL_3](https://github.com/user-attachments/assets/dde9ad43-6498-42cb-b10c-516f69f51ca7)
![SQL_4](https://github.com/user-attachments/assets/e3f44909-a2f2-4eb1-be49-9680a042c35d)

## 🛠 Tools & Technologies Used
🔹 SQL Development: DBeaver Enterprise

🔹 Database Design: [draw.io](draw.io)

🔹 Database Platform: PostgreSQL

🔹 Code & Version Control: GitHub
