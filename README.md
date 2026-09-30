# Pax - Telemetria Humana para Mobilidade Urbana 🚌⚡

Este repositório contém o protótipo funcional da interface mobile do **Pax**, uma solução GovTech de inteligência de dados construída sob o modelo **DePIN** (Decentralized Physical Infrastructure Network). O objetivo é resolver a "cegueira situacional" do transporte público, transformando o passageiro no principal sensor de dados da cidade em tempo real.

## ⚠️ O Problema

O Centro de Controle Operacional (CCO) da prefeitura (ex: URBS em Curitiba) possui um controle de ponta sobre a infraestrutura estática:
- Eles sabem exatamente onde o ônibus está via GPS.
- Eles sabem se o itinerário está no horário.
- **Mas existe um ponto cego crítico: eles não sabem o que acontece com as pessoas lá dentro em tempo real**.

A gestão atual depende de dados de catraca, que registram embarques com defasagem e sem saber onde a pessoa desce. Outra dependência são as pesquisas anuais de satisfação por amostragem, como o QualiÔnibus. O resultado é a ineficiência: fiscais de terminal trabalhando às cegas e passageiros enfrentando viagens desconfortáveis e sem previsibilidade.

## 💡 A Solução (Pax)

O Pax evoluiu de um simples mapeador de superlotação para uma rede DePIN de telemetria da **experiência completa da viagem**. Nós transformamos o smartphone do cidadão em um sensor contínuo, estruturado em três pilares principais:

1. **Telemetria da Experiência (Fricção Zero):** O reporte leva menos de 10 segundos e exige apenas 2 ou 3 toques intuitivos na tela. O usuário não apenas relata a lotação, mas avalia o conforto a bordo, a dirigibilidade, o funcionamento do ar-condicionado ou ruído e os gargalos de embarque e desembarque. O passageiro deixa de ser passivo e vira um auditor ativo da qualidade da cidade.
2. **Coleta Gamificada e Antifraude:** O cidadão recebe uma micro-recompensa instantânea em tokens PAX a cada validação confirmada. Para evitar fraudes, o sistema utiliza mecanismos de *Proof of Location* (Prova de Localização), exigindo que o GPS do aparelho esteja dentro da cerca eletrônica (geofencing) do veículo em movimento. Além disso, um alerta só é classificado como confiável quando há convergência e algoritmo de consenso de múltiplos reportes concorrentes no mesmo carro.
3. **Integração B2G (Business to Government):** Os dados gerados pelo aplicativo são cruzados com os arquivos abertos de telemetria e itinerários em formato JSON da URBS. O painel do CCO passa a receber alertas preditivos de saturação de linha e relatórios de conforto contínuos, permitindo o envio de ônibus de reforço e remanejamento operacional.

## 🛠️ Tecnologias Utilizadas (Protótipo)

Nesta fase de ideação e validação de interface, o app foi construído de forma enxuta para rodar diretamente no navegador:
- **HTML5 & CSS3**
- **Tailwind CSS** (via CDN para estilização rápida e design system próprio)
- **React 18** (UMD sem build process, utilizando Hooks para controle de estado)

## 🚀 Como visualizar

O protótipo está hospedado via GitHub Pages e pode ser testado diretamente no link abaixo:
👉 **[Acessar Protótipo do Pax](https://jeancarlocorreia.github.io/pax_app/)**

### 📱 Fluxo de Teste Interativo

Siga o passo a passo abaixo para simular a experiência completa do passageiro:

1. **Detectar e Iniciar Viagem:** 
   Na aba **"Detectar"**, clique em `Simular GPS` ou abra o filtro para selecionar a linha detectada (ex: *Interbairros IV*). Em seguida, clique em **Iniciar viagem**.

2. **Avaliar Lotação:** 
   O aplicativo mudará para a aba **"Viagem"**. Classifique o nível de ocupação atual do veículo selecionando entre: *Vazio, Baixa, Média, Cheio* ou *Lotado*.

3. **Detalhamento Extra (Condicional):** 
   Se a opção **Lotado** for selecionada, o sistema exigirá validações qualitativas adicionais. Responda se o fundo do ônibus está cheio e indique a quantidade estimada de pessoas em pé.

4. **Reportar e Receber Recompensa:** 
   Toque no botão **Reportar lotação** para enviar o status da viagem em tempo real ao painel de controle. Neste momento, o sistema simula o recebimento da sua primeira micro-recompensa na carteira digital.

5. **Finalizar Trajeto:** 
   Ao chegar ao seu destino e encerrar o trajeto físico, clique no botão vermelho **Descer** na seção inferior da tela.

6. **Avaliar Experiência Geral:** 
   Automaticamente, o app mudará para a aba **"Avaliar"**. Selecione os **Pontos positivos** (ex: *Ar condicionado, Limpo*) e os **Problemas** (ex: *Direção brusca, Superlotado*) enfrentados durante a jornada. Por fim, clique em **Enviar avaliação** para confirmar sua auditoria e coletar a recompensa final on-chain (ex: `+ 0.50 PAX`).
