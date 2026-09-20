# M4 – Bugjakt: bevisa buggen med ett test

## 1. Testet som reproducerar buggen

Testet i `backend/tests/test_bugjakt.py` reproducerar följande scenario:

1. Skapar en item med texten `milk`.
2. Skapar en item med texten `bread`.
3. Tar bort `bread`.
4. Hämtar `/api/items/stats`.
5. Förväntat resultat är 1 item och totalt 4 tecken.

 Och testet kördes innan buggen fixades:

```text
F [100%]

E       AssertionError: assert {'count': 1, 'total_characters': 9} == {'count': 1, 'total_characters': 4}

Differing items:
{'total_characters': 9} != {'total_characters': 4}

1 failed, 1 warning in 0.09s
```

Så detta visar att buggen kunde reproduceras med ett automatiskt test.
Efter att `bread` togs bort var antalet items korrekt, men `total_characters` var fortfarande 9 istället för 4.

## 2. Varför kunde buggen finnas kvar?

Den vanliga testsviten var grön före ändringen, men den innehöll inte testet för just detta scenario.

Vid kodgranskning kunde det också vara svårt att upptäcka problemet eftersom `delete_item()` tog bort item från listan, men inte uppdaterade `_total_characters`.

## 3. Fix

Problemet fanns i `delete_item()` i `backend/app/main.py`.

När en item tas bort minskas nu `_total_characters` med längden på den borttagna itemens text.

Efter fixen kördes samma test igen och resultatet blev:

```text
. [100%]

1 passed, 1 warning in 0.05s
```

## 4. Vad kunde ha förhindrat buggen?

Ett automatiskt test för att skapa och sedan ta bort en item hade kunnat upptäcka problemet tidigare.

Testet visar också varför det är viktigt att testa både skapande och borttagning av data när applikationen har statistik som bygger på datan.

## 5. Bevis

Skärmbild från det röda testet före fixen bifogas till denna inlämning.
