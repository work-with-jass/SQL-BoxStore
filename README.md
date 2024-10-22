# SQL BoxStore

## Tables Created
1. people TABLE (p)
2. geo_address_type TABLE (gat)
3. geo_country TABLE (gco)
4. geo_region TABLE (grg)
5. geo_towncity TABLE (gtc)
6. people_employee TABLE (pe)
7. manugacturer TABLE (m)

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
