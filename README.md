# Bases curadas — Validador de Lote RTC

Canal público de distribuição das closures XSD NF-e/NFC-e curadas para o
Validador de Lote RTC. Este repositório não recebe XMLs de usuários.

`stable.json` é assinado com Ed25519. Cada release é imutável, tem sequência
monótona e aponta para um ZIP cujo SHA-256 é conferido pelo aplicativo antes
da extração. A chave privada de assinatura não pertence a este repositório.

## Publicação

1. Revisar a closure XSD e sua proveniência.
2. Criar ZIP imutável em `releases/` e calcular SHA-256.
3. Incrementar `releaseSequence`, atualizar o payload `signed` e assinar sua
   serialização canônica.
4. Revisar o commit e publicar no branch `main`.

Nunca edite uma release publicada ou reutilize `releaseSequence`.
Canal curado e assinado de schemas NF-e/NFC-e do Validador de Lote RTC
