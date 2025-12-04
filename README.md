# sistema de rounds

Os rounds serão feitos desse jeito **:**

crie uma scoreboard dummy chamada locallevel
``` mcfunction
/scoreboard objectives add locallevel dummy
```

``` mcfunction
/scoreboard objectives add tpplevel dummy
```

``` mcfunction
/scoreboard objectives add worldlevel dummy
```

Verifique se o player tem a scoreboard **locallevel** de um certo level, se sim o player\
será teleportado para um armor stando com a scoreboard **tpplevel** sendo o mesmo nivel do player

``` mcfunction
/exe
```

