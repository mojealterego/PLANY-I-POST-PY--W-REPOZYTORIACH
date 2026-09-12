# Audyt 95 — mailtm-client

## Stan
AUDYT ZAKOŃCZONY — lekki wrapper Python dla MailTM API.

## Ustalenia
README opisuje automatyczne tworzenie disposable-mail accounts, losowanie credentials, JWT login oraz odczyt inboxu. Deklaruje `requests` jako podstawową zależność i MIT. Instrukcja instalacji zawiera placeholder `yourusername`, więc publikacja pakietu/dokumentacja nie są finalne.

## Ryzyka
- disposable email może mieć zastosowania nadużyciowe;
- JWT/session handling;
- pobieranie pełnej treści wiadomości;
- brak potwierdzonego rate limiting/error model;
- placeholderowe dane repozytorium w dokumentacji.

## Priorytet
ŚREDNI.

## Kolejność prac
API contract → timeout/retry/rate limit → auth token lifecycle → parsing/size limits → test fixtures → compliance/abuse policy → package metadata → Polish docs.

## Kryterium zakończenia
Klient jest deterministyczny i odporny na błędy API, nie automatyzuje nadużyć, a dokumentacja i metadane pakietu odpowiadają rzeczywistemu repozytorium.