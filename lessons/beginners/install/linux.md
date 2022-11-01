# Instalace Pythonu na Linux

Nainstalovat Pyhon na Linux je většinou jednoduché.
Jen existuje spousta druhů Linuxu a máme s ním největší zkušenosti,
tak jsou tyhle instrukce trochu delší.
Nezalekni se – většinu sekcí pravděpodobně přeskočíš. :)

## Instalace Pythonu 3

Na Linuxu většinou Python 3 už bývá. Abys to zkontroloval{{a}}, spusť
v [příkazové řádce]({{ lesson_url('beginners/cmdline') }}) příkaz:

```console
$ python3 --version
```

Objeví-li se „Python“ a číslo verze (např. `Python 3.6.6`)
a verze je 3.6 nebo vyšší, máš nainstalováno.
Přejdi na další sekci, [kontrolu `tkinter`](#check-tkinter).

Objeví-li se „Python“ a verze 3.5 nebo nižší,
{% if var('coach-present') -%}
poraď se s koučem.
{%- else -%}
aktualizuj systém (nebo se poraď s někým, kdo to umí) a zkus to znovu.
{%- endif %}

Objeví-li se `bash: python3: command not found` nebo podobná chyba,
doinstaluj Python.
Konkrétní příkaz záleží na distribuci:

* **Fedora**:
  {% filter markdown(inline=True) %}
  ```console
  $ sudo dnf install python3
  ```
  {% endfilter %}
* **Ubuntu**:
  {% filter markdown(inline=True) %}
  ```console
  $ sudo apt-get install python3
  ```
  {% endfilter %}

Používáš-li jinou distribuci, doufám, že instalovat programy už umíš.


{{ anchor('check-tkinter') }}
## Kontrola Tkinter

Některé linuxové distribuce obsahují standardně jen část celkové funkčnosti
Pythonu.
Konkrétně knihovnu `tkinter` (která umožňuje např. kreslit „želví obrázky“)
často musíme nainstalovat zvlášť.
Abys zjistil{{a}}, jestli je už je nainstalovaná, zadej příkaz:

```console
$ python3 -m tkinter
```

Objeví-li se okýnko, je všechno v pořádku.

Jestli ne, modul `tkinter` ještě nainstaluj:

* **Fedora**:
  {% filter markdown(inline=True) %}
  ```console
  $ sudo dnf install python3-tkinter
  ```
  {% endfilter %}
* **Ubuntu**:
  {% filter markdown %}
  ```console
  $ sudo apt-get install python3-tk
  ```
  {% endfilter %}

Používáš-li jinou distribuci, musíš si správné jméno balíčku najít na Internetu.