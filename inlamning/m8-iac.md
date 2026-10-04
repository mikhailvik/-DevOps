# M8 – Infrastructure as Code med Terraform

## Steg 4 – Första terraform apply
Terraform skapade infrastrukturen i cPouta från Terraform-konfigurationen.

![Terraform apply](m8-steg4.png)

## Steg 5 – Applikationen fungerar
Applikationen kunde nås via den nya floating IP-adressen och nip.io-adressen.

![Applikationen i webbläsaren](m8-steg5.png)

## Steg 6 – M7-resurser borttagna
Den manuellt skapade M7-instansen togs bort efter att M8-miljön hade verifierats.

![Instances efter borttagning av M7](m8-steg6.1.png)

Den gamla floating IP-adressen från M7 frigjordes. Endast M8-adressen finns kvar.

![Floating IP efter borttagning av M7](m8-steg6.2.png)

## Steg 7 – Terraform state
Jag kontrollerade Terraform state och såg resurserna som Terraform hanterar.

![Terraform state list](m8-steg7.png)

## Steg 8 – Rebuild med samma floating IP
VM-instansen byggdes om med Terraform. Floating IP-adressen var samma före och efter rebuild.

![Samma floating IP före och efter rebuild](m8-steg8.png)