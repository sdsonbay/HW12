# HW12

--1
SELECT COUNT(*) FROM film WHERE length > (SELECT AVG(length) FROM film);
--2
SELECT COUNT(*) FROM film WHERE rental_rate = (SELECT MAX(rental_rate) FROM film);
--3
SELECT COUNT(*) FROM film WHERE rental_rate = (SELECT MIN(rental_rate) FROM film) OR replacement_cost = (SELECT MIN(replacement_cost) FROM film);
--4
SELECT first_name, last_name, (SELECT COUNT(*) FROM payment WHERE payment.customer_id = customer.customer_id) AS order_count FROM customer ORDER BY order_count DESC;
