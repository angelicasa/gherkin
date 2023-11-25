# Curso de Gherkin: Do Básico ao Avançado

Este repositório contém práticas e informações relacionadas ao curso "Gherkin: Do Básico ao Avançado", ministrado pela instrutora Priscila Caimi na plataforma Qualiters Club. 

![diploma curso gherkin](https://github.com/angelicasa/gherkin/assets/107443453/94edaa98-4507-4abf-95ad-aff44b04cf45)

# Fluxo de Certificação no Curso Gherking

## Validação positiva

Given que estou logada na plataforma
And matriculada no curso Gherking do básico ao avançado
When finalizo o meu curso
Then tenho o meu certificado

## Validação negativa e uso do "but"

Given que estou logada na plataforma
And matriculada no curso Gherking do básico ao avançado
When assisto as aulas
Then não tenho meu certificado disponível
But possuo aulas assistidas

## Feature: Emissão do certificado de conclusão

Como aluna da plataforma,
Eu gostaria que, ao completar o curso,
O sistema emita um certificado
Para que eu possa comprovar o meu conhecimento técnico.

## Colocando contexto

Background: Estar matriculada no curso Gherking do básico ao avançado
Given que estou logada na plataforma
And matriculada no curso Gherking do básico ao avançado

## Primeira validação

Scenario: Emissão de certificado
When finalizo o meu curso
Then tenho o meu certificado emitido

## Segunda validação

Scenario: Curso em andamento
When assisto as aulas
Then não tenho meu certificado disponível
But possuo aulas assistidas

## Esquema de cenário

Scenario Outline: Emissão de certificado
And matriculada no curso <nomeCurso>
When finalizo o meu curso
Then tenho o meu certificado emitido

## 3 massas de teste

Examples:
    | nomeCurso                              | 
    | "Gherking do básico ao avançado"       | 
    | "7 princípios do Teste de software"     | 
    | "Operadores lógicos"                   | 

## Alteração de step no background 

Background: Estar matriculada no curso Gherking do básico ao avançado
Given estou logada na plataforma
And possuo matrícula ativa
When finalizo o meu curso
Then tenho o meu certificado emitido