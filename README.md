# Backend

## NuGets:
 - Microsoft.EntityFrameworkCore (8.0.23)
 - Microsoft.EntityFrameworkCore.Design (8.0.23)
 - Microsoft.EntityFrameworkCore.Tools (8.0.23)
 - Microsoft.EntityFrameworkCore.Sqlite (8.0.23)

## Context osztály létrehozása:

public class DatabaseContext : DbContext
{
  public DatabaseContext(DbContextOptions<DatabaseContext> options) : base(options) {}

  public DbSet<Model> Models {get;set;}
}

## Appsettings.json: 
"ConnectionStrings": {
  "DatabaseContext": "Data Source=SQLiteDatabaseContext.db"
}

## Program.cs:
builder.Services.AddDbContext<PoolCarContext>(  
  db => db.UseSqlite(builder.Configuration.GetConnectionString("PoolCarContext"))); 

 
# Bootstrap osztályok

## .container

### Használat

```html
<div class="container">
    Tartalom
</div>
```

### Leírás

A `container` osztály középre rendezi az oldalon lévő tartalmat, és maximális szélességet állít be. Ez a Bootstrap egyik legalapvetőbb layout eleme. Reszponzív viselkedést biztosít, tehát különböző kijelzőméreteken automatikusan változtatja a szélességet.

---

## .container-fluid

### Használat

```html
<div class="container-fluid">
    Tartalom
</div>
```

### Leírás

A `container-fluid` a teljes képernyőszélességet kihasználja. Akkor használjuk, amikor az elemnek végig kell érnie az egész oldalon, például bannereknél vagy teljes szélességű szekcióknál.

---

## .row

### Használat

```html
<div class="row">
</div>
```

### Leírás

A `row` Bootstrap sorokat hoz létre a grid rendszerben. A sorokba kerülnek az oszlopok (`col`). A Bootstrap 12 oszlopos rendszere csak `row` elemen belül működik megfelelően.

---

## .col

### Használat

```html
<div class="col">
    Tartalom
</div>
```

### Leírás

A `col` automatikusan egyenlő méretű oszlopokat készít. Ha több `col` elem van egy sorban, akkor azok egyenlően osztoznak a rendelkezésre álló helyen.

---

## .col-6

### Használat

```html
<div class="col-6">
    Tartalom
</div>
```

### Leírás

A `col-6` az adott elemet a sor felére méretezi. Mivel a Bootstrap 12 oszlopos rendszert használ, a 6 oszlop pontosan 50%-os szélességet jelent.

---

## .col-md-6

### Használat

```html
<div class="col-md-6">
    Tartalom
</div>
```

### Leírás

A `col-md-6` közepes kijelzőmérettől kezdve 50%-os szélességet ad az elemnek. Mobiltelefonon teljes szélességű marad, tablettől vagy nagyobb kijelzőn viszont két oszlop jelenik meg egymás mellett.

---

## .d-flex

### Használat

```html
<div class="d-flex">
</div>
```

### Leírás

A `d-flex` bekapcsolja a Flexbox rendszert. Ez lehetővé teszi az elemek egyszerű igazítását és elrendezését vízszintesen vagy függőlegesen.

---

## .justify-content-center

### Használat

```html
<div class="d-flex justify-content-center">
</div>
```

### Leírás

A `justify-content-center` vízszintesen középre igazítja a flex elemeket. Gyakran használják gombok, kártyák vagy menüpontok középre rendezésére.

---

## .justify-content-between

### Használat

```html
<div class="d-flex justify-content-between">
</div>
```

### Leírás

A `justify-content-between` a flex elemeket a két szélső oldalra helyezi. Nagyon gyakori navbarok és fejléc elrendezések készítésénél.

---

## .align-items-center

### Használat

```html
<div class="d-flex align-items-center">
</div>
```

### Leírás

Az `align-items-center` függőlegesen középre igazítja a flex elemeket. Akkor hasznos, amikor egy elemnek pontosan középen kell elhelyezkednie.

---

## .text-center

### Használat

```html
<h1 class="text-center">
    Cím
</h1>
```

### Leírás

A `text-center` középre igazítja a szöveget. Gyakran használják címeknél, gomboknál és különböző tartalmi elemeknél.

---

## .text-white

### Használat

```html
<p class="text-white">
    Szöveg
</p>
```

### Leírás

A `text-white` fehér színűvé alakítja a szöveget. Sötét háttér esetén használják az olvashatóság javítására.

---

## .bg-dark

### Használat

```html
<div class="bg-dark">
</div>
```

### Leírás

A `bg-dark` sötét háttérszínt állít be. Leginkább navbaroknál, footereknél vagy modern sötét dizájn kialakításánál használják.

---

## .bg-primary

### Használat

```html
<div class="bg-primary">
</div>
```

### Leírás

A `bg-primary` Bootstrap alapértelmezett kék háttérszínét alkalmazza. Fontos elemek kiemelésére szolgál.

---

## .m-3

### Használat

```html
<div class="m-3">
</div>
```

### Leírás

Az `m-3` külső margót ad az elem minden oldalára. A szám a margó méretét jelöli 0 és 5 között.

---

## .p-3

### Használat

```html
<div class="p-3">
</div>
```

### Leírás

A `p-3` belső térközt ad az elemnek. Segít abban, hogy a tartalom ne tapadjon közvetlenül az elem széléhez.

---

## .btn

### Használat

```html
<button class="btn">
    Gomb
</button>
```

### Leírás

A `btn` Bootstrap gombstílust ad az elemnek. Minden Bootstrap gomb alapja ez az osztály.

---

## .btn-primary

### Használat

```html
<button class="btn btn-primary">
    Küldés
</button>
```

### Leírás

A `btn-primary` Bootstrap alapértelmezett kék gombját készíti el. Általában fő műveletekhez használják.

---

## .btn-danger

### Használat

```html
<button class="btn btn-danger">
    Törlés
</button>
```

### Leírás

A `btn-danger` piros színű gombot hoz létre. Veszélyes vagy törlési műveletek jelölésére szolgál.

---

## .card

### Használat

```html
<div class="card">
</div>
```

### Leírás

A `card` modern kártya komponens létrehozására szolgál. Profilok, termékek és információs blokkok készítésére használják.

---

## .card-body

### Használat

```html
<div class="card-body">
    Tartalom
</div>
```

### Leírás

A `card-body` a kártya belső tartalmát tárolja. Szövegek, képek és gombok elhelyezésére használható.

---

## .shadow

### Használat

```html
<div class="shadow">
</div>
```

### Leírás

A `shadow` árnyékot ad az elemnek. Modern és kiemelt megjelenést biztosít.

---

## .rounded

### Használat

```html
<div class="rounded">
</div>
```

### Leírás

A `rounded` lekerekített sarkokat ad az elemnek. Modern dizájnoknál nagyon gyakran használják.

---

## .img-fluid

### Használat

```html
<img class="img-fluid">
```

### Leírás

Az `img-fluid` reszponzív képet készít. A kép automatikusan igazodik a szülőelem méretéhez és nem lóg ki kisebb kijelzőkön sem.

---

## .table

### Használat

```html
<table class="table">
</table>
```

### Leírás

A `table` Bootstrap stílust ad a táblázatoknak. Szebb és modernebb megjelenést biztosít.

---

## .table-striped

### Használat

```html
<table class="table table-striped">
</table>
```

### Leírás

A `table-striped` váltakozó háttérszínű sorokat készít a táblázatban, ami javítja az olvashatóságot.

---

## .form-control

### Használat

```html
<input class="form-control">
```

### Leírás

A `form-control` modern Bootstrap stílust ad az input mezőknek. Reszponzív és egységes kinézetet biztosít.

---

## .navbar

### Használat

```html
<nav class="navbar">
</nav>
```

### Leírás

A `navbar` navigációs sáv létrehozására szolgál. Bootstrapben ez az egyik leggyakrabban használt komponens.

---

## .alert

### Használat

```html
<div class="alert alert-success">
    Sikeres mentés
</div>
```

### Leírás

Az `alert` figyelmeztető vagy információs üzenetek megjelenítésére szolgál. Több színváltozata is van, például success, danger vagy warning.

---

## .w-100

### Használat

```html
<div class="w-100">
</div>
```

### Leírás

A `w-100` 100%-os szélességet ad az elemnek. Gyakran használják teljes szélességű gombok vagy blokkok készítésére.

---

## .d-none

### Használat

```html
<div class="d-none">
</div>
```

### Leírás

A `d-none` teljesen elrejti az elemet az oldalon. Reszponzív kombinációkban is gyakran használják.
