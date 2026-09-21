# Pint-OS — Alarm Clock

Implementação da atividade **Alarm Clock** do Pint-OS.

## Objetivo

Corrigir o problema de **busy wait** existente na função `timer_sleep()`, evitando que a thread fique executando enquanto aguarda a passagem do tempo.

## Implementação

A solução foi desenvolvida **a partir da estrutura já existente do Pint-OS**, realizando alterações no código de threads e temporizador para:

* Suspender a thread durante o período de espera;
* Controlar as threads que estão dormindo;
* Liberar a thread após o número de ticks solicitado;
* Eliminar o uso de **busy wait**.

## Escopo

Foi implementada **somente a primeira problemática da atividade: Alarm Clock / remoção do busy wait**.

A implementação mantém a estrutura original do Pint-OS, modificando apenas os componentes necessários para solucionar o problema.
