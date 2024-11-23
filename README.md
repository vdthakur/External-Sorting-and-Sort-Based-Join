# External Sorting and Sort-Based Join

This repository contains Python programs to implement two database operations: **External Sorting** and **Sort-Based Join**. Both programs work with large CSV files and efficiently manage memory constraints.

---

## 1. External Sorting

### Description
The `ext_sort.py` program sorts a large CSV file containing a table of products by product name using **External Sorting**. The program assumes:
- Each page/block holds 2 rows.
- A total of 3 pages are available:
  - 1 page is used for sorting.
  - All 3 pages are used during the merging process.

### Execution Format
```bash
python3 ext_sort.py product.csv product_sorted.csv
```

## 2. Sort-Based Join

### Description

The `ssb_join.py` program performs a **Sort-Based Join** between two large CSV files:
- The first file (`product_sorted.csv`) contains a table of products.
- The second file (`maker_sorted.csv`) contains a table mapping products to companies.

The program:
1. Sorts both input tables.
2. Merges the sorted tables to perform the join operation.

### Execution Format
```bash
python3 ssb_join.py product_sorted.csv maker_sorted.csv joined_data.csv
```
