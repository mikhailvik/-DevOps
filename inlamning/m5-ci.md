# M5 – CI

## Steg 2 – Röd CI-check

Jag lade medvetet till en oanvänd `json`-import. CI blev röd och PR kunde inte mergas.

![M5 Steg 2](m5-steg2.png)

## Steg 3 – Fix och grön CI-check

Jag tog bort den oanvända importen. CI blev grön och PR kunde mergas.

![M5 Steg 3](m5-steg3.png)

## Steg 4 – Manuell körning av CI

Jag lade till `workflow_dispatch` och startade CI manuellt på `main`. Workflow-körningen lyckades.

![M5 Steg 4](m5-steg4.png)
