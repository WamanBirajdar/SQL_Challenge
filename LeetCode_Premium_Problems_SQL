# Advanced SQL
# 603. consecutive available seats
```
SELECT w.seat_id
FROM 
	(SELECT 	*, 
			LEAD(free) over(ORDER BY seat_id) AS next_seat,
			LAG(free) over(ORDER BY seat_id) AS previous_seat
	FROM Cinema) AS w
WHERE 	w.free = 1 AND w.next_seat = 1
OR 		w.free = 1 AND w.previous_seat = 1
ORDER BY seat_id;
```
