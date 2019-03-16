```
SELECT m.id, m.title, coalesce(sum(r.number_of_tickets), 0) AS sold_tickets
FROM movies AS m
LEFT JOIN reservations AS r
ON m.id = r.movie_id
GROUP BY m.id, m.title
ORDER BY sold_tickets DESC
```
