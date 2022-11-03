# První program

```pycon
>>> 3 + 4
8
```

Psaní příkazů přímo v Pythonu, <em>interaktivně</em>,
má jednu velkou nevýhodu:
to, co napíšeš, se ztratí, jakmile zavřeš okno příkazové řádky.
Na jednoduché výpočty to nevadí, ale až budou tvoje programy složitější,
budeš je potřebovat nějak uložit.

Otevři editor. Můžeš ho mít buď naistalovaný (Instrukce jsou [zde]({{ lesson_url('beginners/install-editor') }}) nebo použij repl.com. 

V něm vytvoř nový soubor, do kterého napiš následující text:

```python
print("Ahoj světe!")
```

Pak soubor ulož jako `ahoj.py`:


Pokud máš v ukládacím okýnku možnost zvolit *kódování*, zvol `UTF-8`.
Můžeš–li zvolit typ souboru, zvol `.py` nebo „všechny soubory“.

## Spuštění

Otevři si příkazovou řádku.
Pomocí `cd` donaviguj do adresáře, kde máš soubory ke kurzům Pythonu.

> [note]
> S příkazovou řádkou jsme se seznámil{{gnd('i', 'y', both='i')}}
> v [minulé lekci](../../beginners/cmdline/), která popisuje i změnu aktuálního
> adresáře pomocí příkazu `cd`.

Na replit.com není třeba se nikam donavigovat, stačí kliknout na záložku `Shell`, ve které se ti otevře příkazová řádka v té správné složce.

Pak a zadej tento příkaz:

```console
$ python ahoj.py
```

Pokud se vypíše hláška `Ahoj světe!`, gratuluji!
Napsal{{a}} jsi svůj první program v Pythonu!

Jestli to nefunguje, zkontroluj, že:

* Jsi ve správném adresáři. Zkus `pwd` (Unix) nebo `cd` (Windows).
  Aktuální adresář musí být ten, do kterého jsi uložil{{a}}
  soubor s programem.
* Soubor se opravdu jmenuje `ahoj.py`.
  Pomocí `ls` (Unix) nebo `dir` (Windows) zkontroluj, že se soubor opravdu
  jmenuje `ahoj.py` a ne třeba `ahoj.py.txt`.
  Jestli ne, ulož ho znovu pod správným jménem.
* Soubor `ahoj.py` obsahuje správný příkaz, včetně všech uvozovek a závorek.
* Znak `$` nezadáváš – v materiálech je proto, aby bylo
  poznat že jde o příkaz příkazové řádky.
  Na `$` (nebo, na Windows, `>`) končí dotaz, který vypíše sám počítač.
  Příkaz, který zadáváš ty, je jen `python ahoj.py`.

A jestli to pořád nefunguje, zeptej se
{% if var('coach-present') -%}
kouče.
{%- else -%}
zkušenějšího programátora. <!-- XXX: where to direct people? -->
{% endif %}


> [style-note] Typografická vsuvka
>
> V Pythonu je většinou jedno, kde napíšeš mezeru. Stejně jako náš příkaz
> `print("Ahoj světe!")` by fungovalo třeba:
>
> ```python
> print      (   "Ahoj světe!"     )
> ```
>
> Je ale zvykem dodržovat určitá pravidla.
> Jako v češtině se po otvírací závorce a za
> ozavírací závorkou nepíše mezera.
> Na rozdíl od češtiny ale mezeru nepiš ani mezi `print` a závorkou.
> „Správně“ je tedy:
>
> ```python
> print("Ahoj světe!")
> ```
>
> V rámci uvozovek má pak každá mezera význam: když napíšeš
> `"    Ahoj      světe!"`, mezery navíc se objeví ve výsledné hlášce.
