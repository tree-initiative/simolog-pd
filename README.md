# SimOLog-PD v1.0 🚌💎

> **Sim**ulador de **O**timização **Log**ística via **P**rogramação **D**inâmica

Este repositório contém o código-fonte e a documentação do software **SimOLog-PD**, desenvolvido como o protótipo computacional e estudo de caso para o artigo científico:  
*"Modelagem Computacional e Otimização Logística no Transporte de Passageiros: Um Estudo de Caso Aplicado ao ENMC 2026 via Programação Dinâmica"*.

O software resolve de forma ótima o problema de Programação Linear Inteira (PLI) voltado para a alocação de frotas rodoviárias heterogêneas na rota Porto Alegre (POA) para Bento Gonçalves (RS).

---

## 🚀 Demonstração Online

A aplicação está publicada e disponível para execução imediata através do GitHub Pages.  
🔗 **Acesse o simulador aqui:** `https://<seu-usuario>.github.io/<nome-do-repositorio>/`

---

## 🧠 Fundamentação Teórica

Diferente de abordagens puramente heurísticas gulosas (*Greedy*), que sofrem de miopia estrutural ao buscarem apenas eficiências locais, o **SimOLog-PD** implementa um algoritmo exato de **Programação Dinâmica** baseado no Princípio de Otimalidade de Bellman para resolver o problema clássico da *Mochila Inversa*.

### Modelo Matemático (PLI)

- **Função Objetivo (Minimização de Custos):**
  \[\min Z = 1850x_1 + 1450x_2 + 1050x_3 + 850x_4 + 450x_5\]
  *(Onde x₁ a x₅ representam, respectivamente, as unidades alocadas de Ônibus 40, Ônibus 30, Micro-ônibus, Van e Carro).*

- **Restrição de Atendimento à Fila:**
  \[40x_1 + 30x_2 + 20x_3 + 15x_4 + 4x_5 \ge N\]
  *(Onde N é o número de passageiros na fila).*

---

## 🛠️ Instruções de Utilização

Como o software foi desenvolvido em arquitetura cliente (*front-end* puro), ele não necessita de servidores ou interpretadores backend (Node.js, Python, etc.).

### Rodando Localmente
1. Faça o download ou clone este repositório:
   ```bash
   git clone https://github.com<seu-usuario>/<nome-do-repositorio>.git
   ```
2. Navegue até a pasta do projeto e abra o arquivo `index.html` diretamente em qualquer navegador moderno (Chrome, Edge, Firefox, Safari).

### Operação da Interface
1. **Controle deslizante de Demanda:** Arraste o *slider* de quantidade de passageiros para alterar o valor de N de 0 a 500. O motor computacional recalculará e atualizará os gráficos instantaneamente.
2. **Cenários Rápidos do Artigo:** Clique em um dos botões do painel superior (*22 passageiros*, *55 passageiros* ou *120 passageiros*) para carregar na mesma hora os dados numéricos discutidos na seção de resultados do artigo do ENMC.
3. **Leitura dos Relatórios:** 
   - A tabela destaca em verde os veículos alocados.
   - O painel de equações reconstrói a matriz do problema dinamicamente.
   - O log na lateral inferior direita descreve os passos exatos de acumulação do algoritmo de Programação Dinâmica.

---

## 🗂️ Estrutura do Projeto

```bash
├── index.html     # Interface do usuário, estilos CSS e motor do algoritmo de PD
└── README.md      # Instruções de uso e documentação técnica (este arquivo)
```

---

## 📜 Licença e Propriedade Intelectual

Este software é um trabalho de pesquisa acadêmica associado ao XXIX Encontro Nacional de Modelagem Computacional. Direitos de propriedade de software protegidos por registro sob codificação de protocolo junto ao INPI.
