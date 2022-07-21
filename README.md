# Patika.Dev_SQL_Odev_6

Merhabalar,

Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

1.film tablosunda bulunan rental_rate sütunundaki değerlerin ortalaması nedir?

2.film tablosunda bulunan filmlerden kaç tanesi 'C' karakteri ile başlar?

3.film tablosunda bulunan filmlerden rental_rate değeri 0.99 a eşit olan en uzun (length) film kaç dakikadır?

4.film tablosunda bulunan filmlerin uzunluğu 150 dakikadan büyük olanlarına ait kaç farklı replacement_cost değeri vardır?

Kolay Gelsin.

# ÇÖZÜMLER


## 1.film tablosunda bulunan rental_rate sütunundaki değerlerin ortalaması nedir?

SELECT AVG(rental_rate) from film ;

## 2.film tablosunda bulunan filmlerden kaç tanesi 'C' karakteri ile başlar?

SELECT COUNT(title) from film 
WHERE title LIKE 'C%' ;

SELECT COUNT(*) from film 
WHERE title LIKE 'C%' ;

## 3.film tablosunda bulunan filmlerden rental_rate değeri 0.99 a eşit olan en uzun (length) film kaç dakikadır?

SELECT MAX(length) from film 
WHERE  rental_rate = 0.99 ;

## 4.film tablosunda bulunan filmlerin uzunluğu 150 dakikadan büyük olanlarına ait kaç farklı replacement_cost değeri vardır?

SELECT COUNT(DISTINCT(replacement_cost)) from film 
WHERE  length > 150 ;

İYİ ÇALIŞMALAR

