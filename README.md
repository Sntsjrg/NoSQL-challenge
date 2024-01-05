# NoSQL-challenge

## UK Food Hygiene Analysis Overview

The UK Food Standards Agency evaluates establishments nationwide, assigning food hygiene ratings. Our objective is to assist Eat Safe, Love magazine by analyzing this data for targeted article recommendations. The process encompasses database setup, updates, and exploratory analysis.

# Part 1: Database and Jupyter Setup

### MongoDB Setup

1. **Data Import:**
   - Import data from `establishments.json` into MongoDB using `NoSQL_setup_starter.ipynb`.

2. **Library and Client Setup:**
   - Import necessary libraries in Jupyter: PyMongo and Pretty Print (pprint).
   - Create a Mongo Client instance.

3. **Database Confirmation:**
   - Confirm setup:
     - List databases in MongoDB to ensure `uk_food` is listed.
     - List collections in the `uk_food` database to ensure `establishments` is present.
     - Display one document from the `establishments` collection using `find_one()` and `pprint`.
   - Assign the `establishments` collection to a variable.

# Part 2: Update Database

4. **Add New Restaurant and Update:**
   - Add "Penang Flavours" to the database.
   - Find and update `BusinessTypeID` for "Restaurant/Cafe/Canteen".
   - Remove Dover Local Authority documents and validate.

5. **Update Number Values:**
   - Use `update_many` to convert latitude, longitude, and `RatingValue`.

# Part 3: Exploratory Analysis

## Question 1: Hygiene Score of 20

- Identify establishments with a hygiene score of 20.
- Use `count_documents()` and `pprint`.
- Convert to a Pandas DataFrame and display.

## Question 2: RatingValue in London

- Find London establishments with `RatingValue` ≥ 4.
- Use `$regex` for London Local Authority.
- Count, `pprint`, and display in DataFrame.

## Question 3: Top 5 RatingValue=5, sorted by Hygiene near "Penang Flavours"

- Identify RatingValue=5 establishments near "Penang Flavours."
- Sort by hygiene, limit to 5, `pprint`, and display in DataFrame.

## Question 4: Establishments with Hygiene Score of 0 by Local Authority

- Build an aggregation pipeline for Local Authority hygiene scores.
- Count, `pprint`, and display top 10 in DataFrame.

## Conclusion

This analysis provides valuable insights for Eat Safe, Love magazine, facilitating focused article planning. The Jupyter notebook and MongoDB setup ensure a seamless exploration and reporting process for editors and food critics.
