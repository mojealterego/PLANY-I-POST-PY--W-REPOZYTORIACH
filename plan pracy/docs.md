# Future AGI Docs — plan pracy

## Status
AUDYT ZAKOŃCZONY — repozytorium dokumentacyjne.

## Stan faktyczny
Źródło dokumentacji Future AGI, zbudowane na Astro, MDX, React islands i Tailwind CSS v4. README opisuje `src/components`, layouts, navigation, pages/docs, plugins, styles, public images i skrypty. Branches main/dev są chronione przez workflow PR; build generuje stronę i indeks Pagefind, istnieje audit-links.

## Ryzyka
- dokumentacja jest silnie zależna od aktualnych API produktów;
- linki i przykłady mogą się dezaktualizować;
- repo zawiera archiwalne snapshoty, które trzeba wyraźnie odseparować od aktualnej dokumentacji.

## Priorytet
ŚREDNI

## Kolejność prac
1. Zweryfikować package manifest, Astro config i workflow deploy.
2. Zbudować automatyczne testy linków, przykładów i frontmatter.
3. Ustalić źródło prawdy dla terminologii i wersji API.
4. Wykonać polonizację tylko jako warstwę dokumentacyjną bez niszczenia upstream semantics.

## Kryterium zakończenia
Build i audit-links przechodzą, dokumentacja ma kontrolowaną wersjonowanie i provenance, a archiwum nie miesza się z produkcyjną treścią.
