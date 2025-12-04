# sistema de rounds

Os rounds serão feitos desse jeito **:**

crie uma scoreboard dummy chamada locallevel 

``` mcfunction
/scoreboard objectives add tpplevel dummy
```

``` mcfunction
/scoreboard objectives add worldlevel dummy
```
``` mcfunction
/scoreboard objectives add levels trigger
```

Verifique se o player tem a scoreboard **locallevel** de um certo level, se sim o player\
será teleportado para um armor stando com a scoreboard **tpplevel** sendo o mesmo nivel do player

``` mcfunction
[...] 
/execute as @e[type=armor_stand,scores={tpplevel=1}] at @s run tp @p[scores{levels=1},limit=1] @s
```
quando o player usar /trigger levels set 1 - levelmax vai dar pq para ele em um armor stand.
Agora spawne zumbis no armor stand fazendo esse commando **:**

``` mcfunction
/execute as @e[type=armor_stand,scores={tpplevel=1}] at @s if scoreboard players @a[limit=1] levels = 1 run summon seumob @s 
```
