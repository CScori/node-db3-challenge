~~~~~~~~~~~~~~~SQL PORTION~~~~~~~~~~~~~~~~
FOREIGN KEY

- if there is a reserved name as a collumn you can [] around the data source
  an identifier that is added to the current table as anumber not full data // join fixes this
  -join fixes this. merges all the data into one temp table by default it is an inner join

select |need info. kvp| as |added name| from |main query| join |needinfotable| as product on |foreign key| = alias

AGGGREGATE FNC
allows groups of data to have other operations on them
-- first we group
--then preform opps
//select count(\*) from orders // similar to saying find the orders and count everything you find that matches

~~~~~~~~~~~~~~~VSC~~~~~~~~~~~~~~~~
SEEDING
--knex seed:make #SeedName
truncate resets the primary key back default
match cullumn name and order for seed data
--knex seed:run
by setting up cleanup file you can just write data seed insertions 0_cleaner

JOINS
in SQL
select p.contents as Message, u.username as PostedBy
from users as u
join posts as p on u.id = p.user_id;
in VSC KNEX
refact sql and wrap in a promise {
.then(
.select('p.contents as Message', 'u.username as PostedBy')
.from('users as u')
.join('posts as p' 'u.id' '=' 'p.user_id')
)
.catch(etc )
}
