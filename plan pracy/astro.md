# Audyt 87 — astro

## Stan
AUDYT ZAKOŃCZONY — repozytorium projektu hermitAI.

## Ustalenia
README opisuje Astro/JSX aplikację AI z Gemini via Vertex AI, Bright Data, MongoDB Atlas Vector Search, JWT auth, email verification, profile/credits oraz RAG-aware ReAct. Główna ścieżka to `/api/ai/chat.js`; są endpointy auth i RAG ingestion. Sekrety obejmują Gemini, Google Cloud, MongoDB, JWT i SMTP.

## Ryzyka
- SSRF/scraping i pobieranie treści z URL;
- LinkedIn/Instagram/Facebook/Amazon/Zillow/Booking data handling;
- auth/JWT/session security;
- credit deduction idempotency;
- izolacja dokumentów przez `userId`;
- provider API keys.

## Priorytet
KRYTYCZNY.

## Kolejność prac
Auth → SSRF/url policy → RAG tenant isolation → tool schema validation → credit transactionality → rate limits → tests/E2E → privacy/retention → deployment.

## Kryterium zakończenia
Żaden URL/tool nie umożliwia wyjścia poza dozwoloną granicę, kredyty są rozliczane atomowo, a dane RAG są izolowane między użytkownikami.