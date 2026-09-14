# Laboratório Quântico — Engenharia Química

Simulação educacional em HTML, CSS e JavaScript para **Química Geral do segundo semestre de Engenharia Química**.

O percurso parte de um fenômeno observável e conduz o estudante à interpretação das equações, dos orbitais, dos números quânticos e da distribuição eletrônica. A proposta é **prever → explorar → calcular → interpretar → verificar**.

## Acesso dos alunos

Endereço previsto após ativar o GitHub Pages:

**https://arigony.github.io/distruicao_eletronica/**

A presença dos arquivos no repositório não significa, por si só, que o site já está publicado. Confira o endereço exibido em **Settings → Pages** após a primeira publicação.

Os alunos acessam a página pelo navegador, sem instalar aplicativos e sem fazer login no GitHub.

## Percurso didático

| Etapa | Pergunta orientadora | Interação e aprendizagem |
| --- | --- | --- |
| 1. Fenômeno | Por que um gás excitado não emite todas as cores? | Previsão e comparação de espectro contínuo com quatro linhas da série de Balmer. |
| 2. Energia | O que a cor permite calcular? | Controle de comprimento de onda, frequência, energia por fóton, energia molar e transições do hidrogênio; exercício numérico com feedback. |
| 3. Onda e incerteza | Podemos acompanhar o elétron como um planeta? | Exploração da relação de de Broglie e do limite de incerteza em função da diferença de potencial e da dispersão da posição. |
| 4. Orbital | Sem trajetória definida, o que podemos prever? | Acumulação de medidas simuladas de posição no estado 1s do hidrogênio. |
| 5. Schrödinger | O que procuramos ao resolver a equação? | Interpretação de Hamiltoniano, função de onda, energia, densidade e probabilidade integrada. |
| 6. Números quânticos | É possível existir um orbital 2d? | Construção de combinações válidas e inválidas; contagem de orbitais e capacidade eletrônica. |
| 7. Distribuição | Como os elétrons ocupam os estados? | Montagem das configurações de O, P, Fe, Fe²⁺, Fe³⁺, Cu e Cu²⁺; transferência para a oxidação do ferro. |

## Como utilizar em aula

1. Peça uma previsão individual antes de apresentar o resultado da simulação.
2. Solicite a justificativa em dupla: “Qual relação física sustenta sua resposta?”.
3. Explore os controles e compare os resultados com a previsão inicial.
4. Nos cálculos, identifique dados, converta unidades e interprete o resultado.
5. Use as respostas incorretas para discutir o raciocínio, em vez de apenas informar a alternativa correta.
6. Finalize com uma explicação escrita: “O que mudou na minha interpretação do elétron?”.

A navegação é livre. As sete verificações registram se houve uma resposta correta em cada etapa; **não constituem uma prova, nota ou medida validada de aprendizagem**. Repetições corretas não somam pontos extras.

A etapa de distribuição é concluída com uma configuração correta; recomenda-se que o professor peça também a comparação entre Fe, Fe²⁺ e Fe³⁺.

## Uso em celular e computador

- Layout em duas colunas que passa a uma coluna em telas estreitas.
- Botões de pelo menos 44 px de altura, acionáveis por toque.
- Menu de etapas com rolagem horizontal.
- Diagramas ajustados à largura disponível.
- Legendas textuais dos espectros para facilitar a leitura no celular.
- Navegação por teclado, indicação de foco e mensagens de feedback acessíveis.
- Números em notação científica com expoentes em sobrescrito.

**Limite da verificação:** a lógica foi testada com DOM e Canvas simulados. Ainda é necessário verificar renderização, toque e leitura em aparelhos reais; não há garantia de compatibilidade universal. Antes de compartilhar com a turma, teste pelo menos um celular Android, um iPhone quando disponível e um computador.

Os gráficos em Canvas têm descrição textual, mas não equivalem a uma representação tátil ou plenamente explorável por leitores de tela.

## Como publicar no GitHub Pages

1. Verifique se `index.html` está na raiz da branch `main`.
2. Abra [Settings → Pages](https://github.com/arigony/distruicao_eletronica/settings/pages).
3. Em **Build and deployment → Source**, escolha **Deploy from a branch**.
4. Escolha a branch **main** e a pasta **/(root)**.
5. Clique em **Save**.
6. Aguarde a publicação e abra o endereço exibido pelo GitHub.

Documentação oficial: [configurar a origem de publicação do GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).

Se houver erro de publicação, consulte a aba **Actions**. Se aparecer uma versão antiga, recarregue a página sem cache ou abra em uma aba privativa.

## Executar sem hospedagem

Baixe `index.html` e abra o arquivo em um navegador com JavaScript habilitado.

O arquivo é autocontido: não utiliza bibliotecas, fontes remotas, CDN, servidor de aplicação ou instalação de pacotes. Uma cópia local pode ser usada sem internet.

O site hospedado não instala um service worker; portanto, a navegação offline pelo endereço público não é garantida.

## Equações utilizadas

- Radiação: `c = λν`; `E = hν = hc/λ`.
- Energia molar dos fótons: `E_molar = N_A hc/λ`.
- Energia hidrogenoide: `E_n ≈ −2,180 × 10⁻¹⁸ Z²/n² J`.
- Transição: `ΔE_átomo = E_final − E_inicial`; `E_fóton = |ΔE_átomo|`.
- De Broglie: `λ = h/p`; para o elétron acelerado do repouso, `λ = h/√(2m_e eU)`.
- Incerteza: `Δx Δp_x ≥ ℏ/2`; `Δv_x ≥ h/(4πm_eΔx)`.
- Schrödinger: `Ĥψ = Eψ`; para uma partícula, `−(ℏ²/2m)∇²ψ + Vψ = Eψ`.
- Probabilidade: `ρ = |ψ|²`; `P(Ω) = ∫_Ω |ψ|² dτ`.
- Orbitais por subnível: `2ℓ + 1`.
- Capacidade eletrônica do subnível: `2(2ℓ + 1)`; da camada: `2n²`.

As constantes utilizadas estão no início do script em `index.html`. Os cálculos mantêm a precisão interna e arredondam os valores exibidos.

## Modelos científicos e limites

### Espectros e transições

A simulação exibe quatro transições da série de Balmer: n = 3, 4, 5 e 6 para n = 2. A posição das linhas é calculada, mas suas intensidades e cores de tela são esquemáticas.

A energia hidrogenoide é adequada ao modelo não relativístico de espécies com um elétron. Nesta implementação, Z = 1. Não são incluídas correções de massa reduzida, estrutura fina ou interações de átomos multieletrônicos.

### Probabilidade do orbital 1s

A nuvem representa resultados independentes de medidas simuladas para sistemas preparados no mesmo estado; **não representa a trajetória de um elétron**.

A amostragem usa a distribuição radial 1s:

`P(r) = 4r² exp(−2r/a₀)/a₀³`.

A variável `r/a₀` é amostrada de uma distribuição Gamma com forma 3 e escala 1/2, com direção isotrópica. As posições tridimensionais são projetadas no plano xz. A imagem não é um corte bidimensional de `|ψ|²`.

Pontos fora da janela de ±6a₀ são contados e não desenhados. O número de medidas pode ser reiniciado.

### Incerteza e de Broglie

Os cálculos de de Broglie são não relativísticos e consideram um elétron inicialmente em repouso. A incerteza exibida é um limite inferior para o desvio-padrão de uma componente da velocidade, e não a velocidade do elétron.

### Ocupação dos orbitais

O quadro representa ocupação, não uma escala de energia. Cada orbital pode estar vazio, conter ↑, conter ↓ ou conter ↑↓.

Pauli é incorporado pela restrição das opções de ocupação. O feedback verifica quantidade de elétrons, distribuição entre subníveis e regra de Hund. Representações com todos os spins desemparelhados para cima ou todos para baixo são aceitas.

Os diagramas d seguem o modelo de átomos/íons livres. O campo dos ligantes em complexos pode alterar a ocupação e o spin.

## Dados e privacidade

A aplicação não solicita nome, e-mail ou identificação e não envia respostas a um servidor. O progresso existe apenas na memória da aba e é reiniciado ao recarregar. Não há banco de dados, analytics ou integração com notas do Moodle.

A hospedagem possui seus próprios registros técnicos de acesso; isso é diferente de a simulação coletar respostas dos estudantes.

## Verificação realizada

Foram executadas **28 verificações de lógica** com DOM/Canvas simulados, além da análise sintática do JavaScript e dos 38 manipuladores de eventos e da conferência de identificadores únicos.

A cobertura inclui:

- navegação entre as sete etapas;
- entrada numérica com vírgula decimal;
- rejeição de resposta vazia e de ordem de grandeza incorreta;
- rejeição de 2d e de mℓ incompatível com ℓ;
- acumulação e reinicialização da nuvem;
- configurações corretas dos sete átomos/íons;
- rejeição de emparelhamento prematuro e de spins desemparelhados não paralelos;
- remoção incorreta de elétrons do ferro;
- alternância dos botões de orbitais;
- contagem única de cada etapa concluída.

Essas verificações não substituem testes visuais em um navegador ou ensaios com a turma.

## Estrutura

- `index.html`: interface, estilos, cálculos, atividades e feedback.
- `README.md`: documentação pedagógica e operacional.
- `LICENSE`: licença MIT já presente no repositório.

## Licença

[MIT](LICENSE). Copyright (c) 2026 ANDRE ARIGONY SOUTO.
