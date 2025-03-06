# Design e Arquitetura de Software 2
> Diogo Mazeika

## Aula 27/02/2025
Trade-off: Escolher entre linguagens e abordagens de acordo com o objetivo de sua aplicação (consistencia, durabilidade, espaço) - basear decisões em dados empiricos

Escalabilidade: Assegurar que uma aplicação consiga se manter mesmo com alta demanda

Automatização: Automatizar processos e recursos de um sistema

IAC: Infraestrutura em forma de codigo

Recursos Descartaveis: Tratar todos os recursos como descartaveis -> torna o serviço mais estavel

## Aula 06/03/2025

Acoplamento:
* Anti-pattern: Banco de dados com alto acoplamento
* Best practice: Banco de dados facilmente substituivel com Elastic Load Balacing (ELB) que permite disponibilidade e garante que o serviço não ficará fora do ar

Arquiteto Frugal: Termo para um arquiteto que se preocupa com custos

Segurança:
* Usar serviços gerenciados (AWS)
* Registrar acesso de recursos
* Isolar partes de sua infraestrutura
* Usar criptografia
* Autenticação de multi-fatores