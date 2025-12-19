E-Commerce API - EasyShop


A Spring Boot REST API for an e-commerce application that allows users to browse products by category , search/filter products , and add their desired item to the cart

==================

Project Overview

This project is a backend API that powers an e-commerce website. It provides endpoints for:
 
 - User authentication and authorization
 - Category management
 - Product management with search filtering
 - Shopping cart functionality

==================

Applications Used 
Java - Programming language

Spring Boot - Application framework

Insomnia - API Tester 

MySQL - Database

JWT - Token-based authentication

Maven - Dependency management

==================

Features Implemented
Phase 1: Categories Management

GET all categories
GET category by ID
POST create new category (Admin only)
PUT update category (Admin only)
DELETE category (Admin only)

Phase 2: Bug Fixes

Bug 1 Fixed: Product search now correctly filters by minimum price

Issue: The minPrice parameter was not being applied in the SQL query
Solution: Added AND (price >= ? OR ? = -1) condition to the search query


Bug 2 Fixed: Product updates no longer create duplicates

Issue: The updateProduct() method was calling create() instead of update()
Solution: Changed productDao.create(product) to productDao.update(id, product) in ProductsController
