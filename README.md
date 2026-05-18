# 🛡️ Análise de Dados para Detecção de Phishing

Este projeto foi desenvolvido como parte do meu processo de preparação e candidatura para uma Iniciação Científica na área de Inteligência Artificial e Análise de Dados. O objetivo principal é analisar heurísticas e parâmetros estruturais de URLs para diferenciar sites legítimos de páginas falsas (*phishing*).

O repositório contém a engenharia de recursos (tradução e tratamento), análise exploratória dos dados e a estruturação inicial para o treinamento de modelos preditivos inteligentes.

---

## 📊 O Dataset e Parâmetros de Análise

Os dados extraídos analisam o comportamento técnico e estrutural das páginas web com base em **30 atributos fundamentais** (mapeados e traduzidos no projeto), além do rótulo final de classificação (`Result`):

| Atributo Original | Tradução / Significado Técnico |
| :--- | :--- |
| `having_IP_Address` | Tem endereço IP direto na URL invés do domínio |
| `URL_Length` | Comprimento total da URL |
| `Shortining_Service` | Uso de serviços de encurtamento de link (ex: bit.ly) |
| `having_At_Symbol` | Presença do símbolo `@` na URL |
| `double_slash_redirecting` | Redirecionamento por barra dupla `//` suspeita |
| `Prefix_Suffix` | Uso de hífen `-` no domínio (comum em sites falsos) |
| `having_Sub_Domain` | Quantidade de subdomínios presentes |
| `SSLfinal_State` | Estado e validação do certificado SSL (HTTPS) |
| `Domain_registeration_length` | Duração e validade do registro do domínio |
| `Favicon` | Carregamento do Favicon de domínios externos |
| `port` | Uso de portas de comunicação não padrão |
| `HTTPS_token` | Presença do termo "https" na parte de texto do domínio |
| `Request_URL` | Proporção de requisições de imagens/objetos externos |
| `URL_of_Anchor` | Links internos (`<a>`) que apontam para fora do domínio |
| `Links_in_tags` | Links externos contidos em tags `<meta>`, `<script>` e `<link>` |
| `SFH` | Server Form Handler (manipulação e envio de dados de formulários) |
| `Submitting_to_email` | Envio de dados coletados diretamente para e-mails |
| `Abnormal_URL` | URL fora dos padrões normais de identidade do host |
| `Redirect` | Contagem de redirecionamentos da página |
| `on_mouseover` | Uso de JavaScript para alterar links na barra de status |
| `RightClick` | Bloqueio do clique direito do mouse via script |
| `popUpWidnow` | Exibição de janelas pop-up invasivas |
| `Iframe` | Uso de tags `<iframe>` invisíveis ou ocultas |
| `age_of_domain` | Idade cronológica do domínio registrado |
| `DNSRecord` | Existência de registro DNS válido para o site |
| `web_traffic` | Volume de tráfego web medido pelo ranking global |
| `Page_Rank` | Classificação do PageRank do domínio |
| `Google_Index` | Se a página já foi indexada pelo buscador do Google |
| `Links_pointing_to_page` | Quantidade de links externos apontando para a página |
| `Statistical_report` | Relatório estatístico de servidores de segurança conhecidos |
| **`Result`** | **Resultado Final (Alvo): Identificação se é Phishing ou Seguro** |

---

## 🛠️ Tecnologias e Ferramentas Utilizadas

* **Python:** Linguagem base para manipulação de dados e computação científica.
* **Jupyter Notebook (`.ipynb`):** Ambiente interativo utilizado para documentar o passo a passo da análise, plotagem de gráficos e testes de hipóteses.
* **Pandas & NumPy:** Manipulação, limpeza, tradução e estruturação matricial do dataset.

---

## 📂 Estrutura do Repositório

```text
├── CódigosApenas/               # Scripts isolados de apoio
├── venv/                        # Ambiente virtual Python isolado
├── analise.ipynb                # Jupyter Notebook principal com a análise exploratória
├── meu_dataset_phishing.csv     # Base de dados com as heurísticas de segurança
README.md                    # Documentação principal do repositório
