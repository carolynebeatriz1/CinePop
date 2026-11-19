# 🎬 CinePop

App de reserva de ingressos de cinema feito em **Python**, com **POO**, banco de dados **SQLite** e interface em **Tkinter**.

Escolha o filme, o horário e a poltrona, e saia com o ingresso pronto, com o código da compra.

## Funcionalidades
- 4 filmes em cartaz e em pré-venda, com 10 sessões (dublado, legendado, 3D e IMAX)
- Mapa da sala com 60 poltronas, e as vendidas aparecem com ×
- Pagamento simulado, com nome e forma de pagamento
- Ingresso no estilo retrô, com código único (ex: CP-K7M2QX)

## Como funciona
O sistema é dividido em 3 serviços, cada um uma classe:
- **Cartaz:** filmes, horários, salas e preços
- **Poltronas:** mostra as ocupadas e reserva as escolhidas
- **Pagamento:** gera o código e registra a compra

A mesma poltrona nunca é vendida duas vezes: a tabela de ingressos tem `UNIQUE(horario_id, poltrona)` e a reserva roda numa transação (tudo ou nada).

Na interface, cada tela é uma classe filha de `Tela` (herança), e cada uma tem o seu próprio `desenhar()` (polimorfismo).

## Como rodar
Precisa só do Python 3 instalado. O Tkinter e o SQLite já vêm com ele.

    python cinepop.py

O banco `cinepop.db` é criado sozinho na primeira vez.

## Tecnologias
Python 3 · Tkinter · SQLite · Programação Orientada a Objetos

---
Feito por **Carolyne Beatriz** · Técnico em Informática (Estácio) · 2026
