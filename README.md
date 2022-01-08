# postgreSQL_odev7
PostgreSQL -  Yedinci ödev - Ilgar Babashli

# _Q1_ 
film tablosunda bulunan filmleri rating değerlerine göre gruplayınız.

# _Ans_
SELECT rating, title from film
GROUP BY rating, title
ORDER BY rating;

# _Q2_ 
film tablosunda bulunan filmleri replacement_cost sütununa göre grupladığımızda film sayısı 50 den fazla olan replacement_cost değerini ve karşılık gelen film sayısını sıralayınız.
# _Ans_
SELECT replacement_cost, COUNT(*) FROM film
GROUP BY replacement_cost
HAVING COUNT(*) > 50;


# _Q3_ 
SELECT store_id, COUNT (*) FROM customer
GROUP BY store_id;

Çıktı:
1	326
2	273

# _Q4_ 
city tablosunda bulunan şehir verilerini country_id sütununa göre gruplandırdıktan sonra en fazla şehir sayısı barındıran country_id bilgisini ve şehir sayısını paylaşınız.
# _Ans_
SELECT country_id, COUNT (*) FROM city
GROUP BY country_id
ORDER BY COUNT(*) DESC;

Çıktı:
country_id - 44	
count - 60
