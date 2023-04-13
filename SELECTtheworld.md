**p1** SELECT name, continent, population FROM world
**p2** SELECT name 
FROM world
WHERE population >= 200000000
**p3** select name, gdp/population
from world
where population >= 200000000
**p4** select name, population / 1000000
from world
where continent = 'South America'
**p5** select name, population
from world
where name in ('France', 'Germany', 'Italy')
**p6** select name
from world
where name like '%United%'
**p7** SELECT name, population, area
FROM world
WHERE area > 3000000 OR population > 250000000
**p8** SELECT name, population, area
FROM world
WHERE (area > 3000000 AND population <= 250000000) OR
(area <= 3000000 AND population >= 250000000)
**p9** SELECT name, ROUND(population/1000000, 2), ROUND(gdp/1000000000, 2)
  FROM world
WHERE continent = 'South America';
**p10** SELECT name, ROUND(gdp/population, -3)
from world
WHERE gdp >= 1000000000000
**p11** SELECT name, capital
FROM world
WHERE LEN(name) = LEN(capital)
**p12** SELECT name, capital
FROM world
WHERE LEFT(name, 1) = LEFT(capital, 1)
AND
name != capital
**p13** SELECT name
FROM world
WHERE name NOT LIKE '% %'
AND name LIKE '%a%' -- at least one 'a'
  AND name LIKE '%e%' -- at least one 'e'
  AND name LIKE '%i%' -- at least one 'i'
  AND name LIKE '%o%' -- at least one 'o'
  AND name LIKE '%u%' -- at least one 'u'