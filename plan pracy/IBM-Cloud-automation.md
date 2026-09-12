# Plan pracy — IBM-Cloud-automation

## Status
AUDYT ZAKOŃCZONY — referencyjny system automatyzacji IBM Cloud w trakcie implementacji.

## Stan faktyczny
README opisuje hierarchię A0–A13, control plane, polityki, pamięć, event fabric, narzędzia, IaC, testy chaos/adversarial oraz bridge ChatGPT. Repozytorium rozdziela symulację od wykonania i wymaga dowodów przed oznaczeniem produkcyjności. Deployment obejmuje IBM Code Engine, Trusted Profiles, sekrety i GitHub Actions.

## Ryzyka
- bardzo szeroka powierzchnia agentów i narzędzi;
- uprawnienia IBM Cloud i mutujące endpointy;
- poprawność approval binding i evidence ledger;
- IaC, sekrety i pipeline CI/CD;
- komponenty badawcze mogą błędnie uzyskać status produkcyjny.

## Priorytet
KRYTYCZNY.

## Kolejność prac
1. Zweryfikować `src/`, policy engine, authority model i tool gateway.
2. Przejrzeć testy kontraktowe, chaos i adversarial.
3. Zweryfikować Terraform/OpenTofu oraz GitHub Actions.
4. Wymusić least privilege, fail-closed i dowody postcondition.
5. Polonizacja dokumentacji bez zmiany semantyki polityk.

## Kryterium zakończenia
Reprodukowalne buildy, zweryfikowane testy bezpieczeństwa, deterministyczne bramki uprawnień i udokumentowane dowody dla każdego twierdzenia produkcyjnego.
