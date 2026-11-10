<div align="center">

**Português** · [English](README.en.md) · [Español](README.es.md)

# Poker MTT BI

**O app onde acompanho meus torneios de poker: painéis, o financeiro do time e um assistente com IA local que responde e lança as coisas por mim.**

<img src="docs/img/resumo-escuro.png" alt="Tela Resumo no tema escuro" width="900">

<sub>Código fechado · imagens com dados fictícios</sub>

</div>

## Por que existe

Jogo torneios online (MTT) todos os dias, em várias contas, dentro de um time. O time tem regras próprias de divisão: makeup, deal, rakeback e meta semanal. Eu controlava tudo em planilha, e conferir se cada pagamento batia virou trabalho de horas.

Hoje eu marco os registros do dia e o app faz o resto. Mostra como estou indo, calcula o que o time me deve e me avisa quando alguma coisa não bate.

## Resumo

O mês num olhar: lucro, ROI, a curva da carreira, o melhor torneio, o resultado por categoria e por conta, e quanto falta para a meta de rake da semana.

<img src="docs/img/resumo-claro.png" alt="Tela Resumo no tema claro" width="900">

## Diário e Torneios

O calendário mostra cada dia jogado e o resultado dele. Clicando num dia aparecem os destaques. Em Torneios fica a lista completa, com busca, filtros e exportação para planilha.

<img src="docs/img/diario.png" alt="Tela Diário" width="900">

<img src="docs/img/torneios.png" alt="Tela Torneios" width="900">

## Financeiro

O app refaz o makeup dia a dia desde o primeiro torneio, com as regras do time de cada época. Mostra a semana atual, as semanas fechadas, os saques recebidos e quanto falta para liberar o rakeback.

<img src="docs/img/financeiro.png" alt="Tela Financeiro" width="900">

## Pool

Colo o relatório diário que o time manda e o app confere os totais, divide a cota de cada jogador e soma o mês.

<img src="docs/img/pool.png" alt="Tela Pool" width="900">

## Assistente com IA local

Um chat dentro do app, com um modelo de linguagem (Qwen, `qwen3.5:4b`) rodando na minha própria placa de vídeo. Não tem custo de API, e nenhum dado sai do computador.

- **Pergunto em vez de procurar:** "quanto lucrei em novembro?", "qual conta mais perdeu em outubro?", "quanto o time já me pagou em setembro?".
- **Lança por mim:** escrevo "caiu 136,20 do diário de 05/11 no Banco Inter" e ele monta o saque. Nada é gravado até eu clicar em **Gravar**.
- **Me avisa:** saque calculado que não caiu, dia da pool sem relatório, registro que precisa de conferência.

O modelo só entende o pedido. Quem faz as contas é o próprio app, então os números que ele mostra são os mesmos das outras telas.

<img src="docs/img/assistente.png" alt="Assistente respondendo uma pergunta e propondo um saque" width="900">

## Grade

A grade semanal de torneios do time, puxada da planilha dele.

<img src="docs/img/grade.png" alt="Tela Grade" width="900">

## Feito com

Construí orquestrando agentes de IA (Claude Code e Gemini), no estilo *vibe coding*: eu defino o que o app faz e as regras, os agentes escrevem o código, e eu confiro e testo no uso de todo dia.

Por baixo: C# e .NET 10 no servidor, React e TypeScript na interface, SQLite como banco e Ollama para o modelo local. Roda inteiro no meu computador, com tema claro e escuro.

---

<sub>Feito por **Yan Camargo** · [LinkedIn](https://www.linkedin.com/in/yan-ca%C3%AA-camargo-38b1002a1/) · © 2026, todos os direitos reservados ([LICENSE](LICENSE))</sub>
