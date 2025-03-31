# azure-ai-sentiment-analysis
Pequeno estudo do *Language StudioAnalyze sentiment and opinions (Version 2023-04-01)*, recurso do Azure AI.

## Procedimento:
Foram testados dois inputs para cada um dos seis tipos de sentenças testadas (positivas, negativas, neutras, mistas, com sarcasmo/ironia e com emoções fortes), totalizando 12 sentenças. Cada resposta foi registrada para análise das porcentagens de sentimento (positivo, negativo ou neutro) e dos graus de confiança classificados pela plataforma.

# Precisão e Sensibilidade da Análise

**Como a IA lida com sarcasmo e ironia?**

Esse foi um dos maiores pontos fracos da plataforma. Em frases irônicas com tom negativo, expressões como *"que ótimo"* e *"para começar bem o dia"* levaram a IA a classificá-las equivocadamente como predominantemente positivas. Isso sugere uma limitação na capacidade do modelo de reconhecer o contexto e nuances do sarcasmo. Além disso, a versão do recurso utilizada (*2023-04-01*) aparenta estar desatualizada em comparação com outras plataformas mais avançadas, como o ChatGPT.

**Frases com sentimentos mistos são identificadas corretamente?**

Não completamente. As frases testadas apresentavam uma combinação equilibrada de sentimentos positivos e negativos, o que deveria resultar em uma classificação proporcional entre esses tons. No entanto, a IA não refletiu essa complexidade:
- Em um dos exemplos, a frase foi classificada como 100% negativa, ignorando a presença de elementos positivos.
- Em outro caso, a IA atribuiu 54% de positividade, 22% de neutralidade e 24% de negatividade, o que demonstra certa variação, mas ainda sem captar a dualidade real do conteúdo.

# Impacto do Contexto
**Frases mistas com palavras emocionalmente carregadas podem ser mal interpretadas? Palavras como “ótimo” e “horrível” influenciam muito o resultado, mesmo sem contexto?**

Sim, e esse fator parece ter sido um dos que mais influenciaram os resultados da IA. O contexto completo da sentença é essencial para uma classificação precisa do sentimento. A plataforma apresentou maior acerto em frases onde não havia ambiguidade, ou seja, quando as palavras-chave correspondiam claramente ao tom emocional da sentença. No entanto, em sentenças mistas, a IA teve dificuldade em equilibrar os diferentes sentimentos, resultando em classificações imprecisas.

# Aplicações Práticas

Mesmo com os resultados mostrando que há dificuldades em identificar sentimentos mistos, ou quando a sentença possui tom pouco formal, as possibilidades de uso com este tipo de ferramenta são inúmeros:

**Monitoramento de popularidade digital**
- A análise de sentimentos pode ser usada para avaliar a percepção pública de figuras políticas, marcas ou influenciadores, analisando comentários e postagens em redes sociais.
- Permite medir oscilações na popularidade ao longo do tempo, identificando crises de imagem ou momentos de maior aceitação.

**Percepção de novos produtos e campanhas**
- Empresas podem utilizar a tecnologia para monitorar reações ao lançamento de produtos, campanhas publicitárias e anúncios, ajustando estratégias com base no feedback do público.
- Identificação rápida de críticas recorrentes para ajustes e melhorias no produto ou serviço.

**Análise de opinião sobre temas polêmicos**
- A tecnologia pode mapear diferentes opiniões sobre debates controversos, como o impacto da IA generativa na arte, mudanças climáticas ou regulamentação de tecnologias emergentes.
- Ajuda a entender padrões de aceitação, resistência e argumentos mais comuns dentro de determinados grupos sociais.

**Comparação de viés midiático**
- Analisando o tom e a linguagem utilizados por diferentes veículos de comunicação ao noticiar o mesmo fato, é possível identificar tendências editoriais e possíveis vieses.
- Ferramenta útil para pesquisas acadêmicas e iniciativas voltadas à transparência na mídia.

### Seguem abaixo, os inputs e outputs deste estudo:

## Sentenças positivas

- Sentença 1 - Hoje foi um dia incrível, porque consegui terminar todas as minhas tarefas."
  
- ![Screenshot 2025-03-30 at 18 11 28](https://github.com/user-attachments/assets/44289725-b254-4c91-9bdb-f797ef010025)

- Sentença 2 - "Adorei conhecer esse novo restaurante, a comida estava maravilhosa!"

- ![Screenshot 2025-03-30 at 18 21 05](https://github.com/user-attachments/assets/a0cb3f66-6aa0-4ef4-abf3-1accf724eaf8)

## Sentenças negativas:
 
- Sentença 3 - "Estou muito frustrado com esse atraso, perdi um compromisso importante."

- ![image](https://github.com/user-attachments/assets/74f0ad21-fbde-425a-9216-619c1c27a59d)


- Sentença 4 - "O atendimento foi péssimo, nunca mais volto aqui."

- ![image](https://github.com/user-attachments/assets/9619d154-fd0e-4bed-b238-c11785620088)

## Sentenças neutras:
- Sentença 5 - "O evento começou às 15h e terminou às 18h."

- ![image](https://github.com/user-attachments/assets/db1e10c2-fc26-4cea-bc7b-a2229db36c18)

- Sentença 6 - "O relatório foi enviado conforme solicitado."

- ![image](https://github.com/user-attachments/assets/c27d5089-7ad5-455e-a826-906ca6c5efe5)

## Sentenças mistas (ambíguas):
- Sentença 7 - "O filme tinha bons efeitos especiais, mas o roteiro deixou a desejar."

- ![image](https://github.com/user-attachments/assets/4068a489-481a-451a-96e1-94b133e43936)

- Sentença 8 - "Gostei da interface do aplicativo, mas ele trava bastante."

- ![image](https://github.com/user-attachments/assets/d41cc06f-ace6-40e5-8762-c55d71cc3145)

## Sentenças contendo sarcasmo/ironia:
- Sentença 9 - "Que ótimo, mais uma reunião desnecessária para o dia!"

- ![image](https://github.com/user-attachments/assets/10a01c1e-41ec-4985-9fac-66522b038fb3)

- Sentença 10 - "Nada como pegar duas horas de trânsito para começar bem o dia."

- ![image](https://github.com/user-attachments/assets/5cea79e1-dc1d-4975-a7a2-50a753c85139)

## Sentenças contendo emoções fortes:
- Sentença 11 - "Estou extremamente animado com essa nova oportunidade!"

- ![image](https://github.com/user-attachments/assets/3d5644b8-33e6-478c-9981-9fde960e7be0)

- Sentença 12 - "Isso é inaceitável! Nunca fui tão mal tratado."

- ![image](https://github.com/user-attachments/assets/b2fa9be3-36f4-449f-b69f-cf1d05047f98)

