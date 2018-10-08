SELECT m.id, m.title, coalesce(sum(r.number_of_tickets), 0) as sold_tickets
from movies m
left join reservations r
on m.id = r.movie_id
group by m.id, m.title
order by sold_tickets desc
