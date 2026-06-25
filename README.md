# Pax - Telemetria Humana para Mobilidade Urbana 🚌⚡

Este repositório contém o protótipo funcional da interface mobile do **Pax**, uma solução de inteligência de dados construída sob o modelo **DePIN** (Decentralized Physical Infrastructure Network) focada em resolver a "cegueira situacional" do transporte público.

## ⚠️ O Problema

O Centro de Controle Operacional (CCO) da prefeitura de Curitiba (URBS) possui um controle de ponta sobre a infraestrutura estática: 
- Eles sabem exatamente onde o ônibus está (GPS).
- Eles sabem se está atrasado (Tabela de Horários).
- **Mas eles não sabem qual é a situação humana dentro do veículo em tempo real.**

A gestão depende de dados de catraca (que chegam com atraso) ou de pesquisas analógicas de amostragem. O resultado é a ineficiência: fiscais de terminal trabalhando no escuro e passageiros sofrendo com superlotação não mapeada.

## 💡 A Solução (Pax)

O Pax atua como uma camada paralela de inteligência de dados qualitativos. Nós transformamos o smartphone do cidadão em um sensor de infraestrutura, com dois pilares principais:

1. **Coleta Gamificada e Tokenizada:** O cidadão relata o nível de lotação, conforto e gargalos nas portas do veículo. Para resolver o desafio da adesão (Cold Start), o usuário recebe uma micro-recompensa instantânea (tokens) a cada validação confirmada via geolocalização e consenso de outros passageiros.
2. **Integração B2G:** Os dados gerados pelo app são cruzados com os arquivos abertos (JSON) da URBS. O painel do CCO passa a receber alertas dinâmicos de "Lotação Crítica", permitindo o envio rápido de carros de reforço e remanejamento operacional.

## 🛠️ Tecnologias Utilizadas (Protótipo)

Nesta fase de ideação e validação de interface, o app foi construído de forma enxuta para rodar diretamente no navegador:
- **HTML5 & CSS3**
- **Tailwind CSS** (via CDN para estilização rápida e design system próprio)
- **React 18** (UMD sem build process, utilizando Hooks para controle de estado)

## 🚀 Como visualizar

O protótipo está hospedado via GitHub Pages e pode ser testado diretamente no link abaixo:
**(Link do seu GitHub Pages vai aqui)**

### Fluxo de Teste:
1. Clique em "Simular GPS" para o sistema detectar em qual linha você está (simulação).
2. Escolha o nível de lotação do ônibus.
3. Se selecionar "Lotado", o sistema exigirá validações qualitativas extras (fundo do ônibus e pessoas em pé).
4. Clique em "Enviar" para simular o recebimento do token PAX na sua carteira digital.

## 👨‍💻 Próximos Passos (Roadmap GovTech)

- [ ] Estruturação do Back-end em Python para cruzamento massivo dos arquivos `.json` da URBS (Tabela de Linha, Veículo e Horários).
- [ ] Desenvolvimento do Dashboard do Gestor (CCO).
- [ ] Definição da arquitetura blockchain para distribuição das recompensas e registro imutável dos dados.
