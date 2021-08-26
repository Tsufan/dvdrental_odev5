# dvdrental_odev5
patika.dev dvdrental örnek veri tabanı ile sorgular ödev5

1) film tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en uzun (length) 5 filmi sıralayınız.
```
SELECT title, length FROM film
WHERE title LIKE '%n'
ORDER BY length DESC
LIMIT 5;
```
![1](sorgu_1.jpg)
***

2 )film tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en kısa (length) ikinci 5 filmi sıralayınız.
```
SELECT title, length FROM film
WHERE title LIKE '%n'
ORDER BY length
OFFSET 5
LIMIT 5;
```
![2](sorgu_2.jpg)
***

3) customer tablosunda bulunan last_name sütununa göre azalan yapılan sıralamada store_id 1 olmak koşuluyla ilk 4 veriyi sıralayınız.
```
SELECT * FROM customer
WHERE store_id IN (1)
ORDER BY last_name DESC
LIMIT 4;
```
![3](sorgu_3.jpg)