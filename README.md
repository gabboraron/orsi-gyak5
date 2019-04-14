# GY5
## Párhuzamosítás

### Szálak
Új szál létrehozása:
````Java
new Thread (() -> {
    //amit a szál csinál
}).run()
````
> Annyi szál van ahányat indítunk +1 a fő szál, a main program!
`t1.join()` nal tudjuk bevárni egy szál lefutását
`new Thread` del hozunk létre új sázlaka
`te.start();` tal indítunk el szálat

**Ne** lőjjük le a szálakat így: ` t.stop();` vagy így `System.exit(123);`

### Szinkrnoizálás szálak között
`synchronized()` leszinkronizálja a két (vagy több) szál között a memóriaterületet (pl: változót) hogy egyszere csak egy szál használja azaz addig feltartja a többieket amíg használjuk.

pl:
````Java
synchronized(txt){
    //műveletek a txt -vel
}
````

Alapból szinkronizált a `thread˙ek között a `println`, így ahhoz nem kell, de a `print`hez igen!

A `synchronized`dal lehet egész blokkot is védeni, így:

````Java
synchronized(this){
    //itt minden szinkronizált lesz
}
````
fájlok: `Parhuzamossag.java`
