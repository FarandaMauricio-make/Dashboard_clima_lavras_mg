# 🌦️ Dashboard do Clima em Lavras - MG

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![Streamlit](https://img.shields.io/badge/Streamlit-1.32-red)
![Altair](https://img.shields.io/badge/Altair-Visualization-orange)
![Status](https://img.shields.io/badge/Status-Funcional-brightgreen)

> **Painel de Inteligência Climática** para monitoramento e análise histórica da cidade de Lavras - MG. O projeto combina previsão horária precisa com uma análise profunda de dados históricos, gerando insights automáticos (Data Storytelling).

## 📋 Sobre o Projeto

Esta aplicação web consome dados meteorológicos da **Open-Meteo API** (uma API open-source de alta precisão) para oferecer uma visão completa do clima local.

Diferente de apps de clima comuns, este dashboard foca na **ciência de dados**: permite cruzar variáveis (temperatura, umidade, vento), exportar relatórios e entender o comportamento climático de períodos passados através de estatísticas automatizadas.

---

## 🚀 Funcionalidades Principais

### 1. 📅 Previsão Horária (Forecast)
- **Monitoramento em Tempo Real:** Dados horários de temperatura, umidade relativa e velocidade do vento.
- **Gráficos Interativos:** Visualização dinâmica com a biblioteca **Altair**, permitindo zoom e seleção de múltiplas variáveis.
- **Exportação:** Download imediato dos dados previstos em CSV ou gráficos em HTML.

### 2. 📆 Histórico Climático
- **Máquina do Tempo:** Seletor de datas personalizável (sidebar) para buscar dados históricos dos últimos dias, meses ou anos.
- **Análise de Extremos:** Gráficos de área para precipitação (chuva) e barras de amplitude térmica (Mínima vs Máxima).
- **Storytelling Automatizado:** O sistema analisa os dados e gera textos automáticos informando o dia mais quente, o mais frio e o mais chuvoso do período selecionado.

### 3. 📊 Engenharia de Dados
- **Cache Inteligente:** Uso de `@st.cache_data` para armazenar requisições por 1 hora, garantindo performance e economizando chamadas de API.
- **Tratamento de Dados:** Conversão automática de timezones e dias da semana em português (Dom, Seg, Ter...).

---

## 🛠️ Tecnologias Utilizadas

* **[Streamlit](https://streamlit.io/):** Framework para construção do Web App interativo.
* **[Altair](https://altair-viz.github.io/):** Biblioteca de visualização estatística declarativa (baseada em Vega-Lite).
* **[Pandas](https://pandas.pydata.org/):** Manipulação, limpeza e estruturação dos dados (ETL).
* **[Requests](https://pypi.org/project/requests/):** Consumo da API REST do Open-Meteo.
* **[Open-Meteo API](https://open-meteo.com/):** Fonte de dados meteorológicos (sem necessidade de API Key).

---

## 📦 Como Rodar o Projeto Localmente

Siga os passos abaixo para executar o dashboard na sua máquina:

1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/SEU-USUARIO/clima-lavras-dashboard.git](https://github.com/SEU-USUARIO/clima-lavras-dashboard.git)
    cd clima-lavras-dashboard
    ```

2.  **Crie um ambiente virtual (Recomendado):**
    ```bash
    python -m venv venv
    # No Windows:
    venv\Scripts\activate
    # No Mac/Linux:
    source venv/bin/activate
    ```

3.  **Instale as dependências:**
    ```bash
    pip install streamlit pandas requests altair
    ```

4.  **Execute o Streamlit:**
    ```bash
    streamlit run dashboard_clima_lavras.py
    ```

---

## 📂 Estrutura de Arquivos

---

## ⚠️ Nota sobre a Localização

O código está configurado com as coordenadas geográficas fixas de **Lavras, Minas Gerais**:
* **Latitude:** -21.245
* **Longitude:** -45.000

*Para adaptar para outra cidade, basta alterar as variáveis `latitude` e `longitude` dentro das funções `get_forecast` e `get_historical` no arquivo `dashboard_clima_lavras.py`.*

---

## 🤝 Contribuição

Sugestões e melhorias são bem-vindas!

1.  Faça um Fork do projeto
2.  Crie uma Branch (`git checkout -b feature/NovaAnalise`)
3.  Faça o Commit (`git commit -m 'Add nova visualização de vento'`)
4.  Push para a Branch (`git push origin feature/NovaAnalise`)
5.  Abra um Pull Request

---

**Desenvolvido com 💙 e Python.**

Você pode acessar o dashboard através do seguinte link: [Clima em Lavras - MG](https://projetos-pessoais-vi7y.onrender.com)




