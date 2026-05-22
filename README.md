# hei 

slkdølads

<img width="960" height="504" alt="image" src="https://github.com/user-attachments/assets/732652f7-26b7-4b19-95a4-561f6a0865a3" />

<img width="960" height="504" alt="image" src="https://github.com/user-attachments/assets/09a3b26a-ea10-4149-a2d4-84e8f6c4e904" />

<img width="960" height="504" alt="image" src="https://github.com/user-attachments/assets/27075965-f795-4392-97e6-bb243c96685e" />

Jeg har startet å lage en pizzabutikk-nettside med Flask som backend og MariaDB som database.

Først installerte jeg Flask i et virtuelt Python-miljø (venv) i VS Code. Deretter laget jeg en Flask-applikasjon i `app.py`.

I Flask laget jeg en route:

```python
@app.route("/")
```

Denne route-en bestemmer hva som skal vises når brukeren går inn på hovedsiden av nettsiden.

Jeg brukte også:

```python
app = Flask(__name__)
```

for å opprette Flask-applikasjonen.

Deretter startet jeg Flask-serveren med:

```python
app.run(debug=True)
```

`debug=True` gjør at serveren oppdaterer automatisk når jeg lagrer filer, noe som gjør utviklingen enklere.

Etter det testet jeg at Flask fungerte ved å vise tekst i browseren.

Senere byttet jeg fra vanlig tekst til HTML ved å bruke:

```python
render_template("INDEX.HTML")
```

Dette gjør at Flask sender en HTML-fil til browseren i stedet for bare tekst.

Jeg opprettet også mappestrukturen som Flask bruker:

* `templates/` for HTML-filer
* `static/` for CSS og andre statiske filer

I `templates/INDEX.HTML` laget jeg en enkel HTML-side med:

* `<html>`
* `<head>`
* `<body>`
* `<h1>`
* `<p>`

Jeg lærte hvordan HTML-tags fungerer, og hvordan Flask kobler backend og frontend sammen.

Deretter installerte jeg MariaDB-driveren i Python med:

```bash
pip install mariadb
```

Målet videre er å koble Flask til MariaDB-databasen på Raspberry Pi-en.

Jeg har allerede laget databasen og tabellene i MariaDB. Neste steg er å hente pizza-data fra databasen med SQL-spørringer som:

```sql
SELECT * FROM pizza;
```

og vise disse dynamisk på nettsiden gjennom Flask.

Jeg har også lært hvordan Flask fungerer som et mellomledd mellom:

* browseren
* backend-koden
* databasen

Flyten blir:

Browser → Flask → MariaDB → Flask → HTML → Browser

Planen videre er:

1. koble Flask til databasen
2. vise pizzaer automatisk fra databasen
3. lage bestillingssystem
4. legge til CSS-design til slutt
