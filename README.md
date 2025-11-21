# ☀️ SolarMaster Pro V11: Simulador de Engenharia e Viabilidade Fotovoltaica

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Status](https://img.shields.io/badge/Status-Stable-green)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

## 📖 Sobre o Projeto

O **SolarMaster Pro** é uma ferramenta desenvolvida em Python para automatizar o processo de dimensionamento técnico e análise financeira de sistemas de energia solar fotovoltaica no Brasil.

Diferente de calculadoras simples, este software integra **Dados Climáticos de Satélite (NASA)**, **Engenharia Elétrica Detalhada** e **Matemática Financeira Avançada** (adaptada à Lei 14.300) para gerar propostas comerciais precisas e seguras em segundos.

---

## 🎯 Contexto: Problema > Solução > Objetivo

### 🛑 O Problema
O mercado de energia solar enfrenta três grandes dores:
1.  **Complexidade Regulatória:** Calcular o impacto da **Lei 14.300** (Taxação do Fio B e Simultaneidade) manualmente é difícil e propenso a erros.
2.  **Insegurança Técnica:** Dimensionamentos feitos "no olho", sem considerar temperatura local ou especificações elétricas (cabos/disjuntores), geram riscos.
3.  **Dificuldade de Venda:** Clientes leigos têm dificuldade em entender métricas complexas como TIR ou kWp.

### 💡 A Solução
Um algoritmo unificado que atua como quatro especialistas:
* **Detetive de Dados:** Busca geolocalização e clima (Irradiação/Temperatura) via API.
* **Engenheiro:** Gera o datasheet técnico (cabos, estrutura, inversor).
* **Consultor Financeiro:** Calcula Payback, VPL, LCOE e protege contra inflação energética.
* **Designer:** Gera dashboards visuais focados em conversão de vendas.

### 🎯 O Objetivo
Democratizar o acesso a projetos de engenharia de alta qualidade, permitindo que orçamentos tecnicamente seguros e financeiramente atraentes sejam gerados instantaneamente.

---

## 🚀 Funcionalidades Principais

### 1. Inteligência de Dados (API NASA POWER)
- Geolocalização automática de qualquer cidade (`Geopy`).
- Consulta em tempo real de Irradiação Solar (HSP) e Temperatura a 2m.
- Cálculo de perda de eficiência térmica baseado no clima local.

### 2. Engenharia Paramétrica (Datasheet)
- Dimensionamento automático de módulos e inversores (com Overloading inteligente).
- Cálculo de **Área de Telhado** e **Sobrecarga Estática** (Peso).
- Especificação automática de **Bitola de Cabos CA** e **Disjuntores** conforme a corrente de saída.
- Definição de arranjo de strings (Série/Paralelo).

### 3. Financeiro "Blindado" (Lei 14.300)
- Cálculo exato da tarifação do Fio B (45% sobre injeção).
- Consideração do **Custo de Disponibilidade** (Taxa Mínima Monofásica/Trifásica).
- Projeção de **Inflação Energética** (Cenários Conservador, Moderado e Crise).
- Simulação de Financiamento (Tabela Price) vs. Pagamento à Vista.

### 4. Dashboard Comercial (Visualização)
- Gráficos gerados via `Matplotlib` com design limpo para propostas.
- Comparativo visual "Antes x Depois".
- Curva de Crescimento Patrimonial.
- Salvamento automático de imagem em alta resolução (`.png`).

---

## 🛠️ Tecnologias Utilizadas

* **Python 3:** Linguagem base.
* **Numpy:** Cálculos vetoriais de alta performance para fluxo de caixa (300 meses).
* **Matplotlib:** Geração de gráficos e dashboards.
* **Requests:** Integração com API REST da NASA.
* **Geopy:** Serviço de geocodificação (Nominatim).

---

## 📦 Como Instalar e Rodar

1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/seu-usuario/solar-master-pro.git](https://github.com/seu-usuario/solar-master-pro.git)
    cd solar-master-pro
    ```

2.  **Instale as dependências:**
    ```bash
    pip install numpy matplotlib requests geopy
    ```

3.  **Execute o simulador:**
    ```bash
    python solar_master.py
    ```

---

## 📊 Exemplo de Saída (Console)

```text
🛠️  RELATÓRIO TÉCNICO DE ENGENHARIA  🛠️
============================================================
🏗️  INFRAESTRUTURA:
    • Área Necessária: 20.8 m²
    • Peso Total: 240 kg (11.5 kg/m²)

⚡  CONEXÃO ELÉTRICA:
    • Inversor: 5.0 kW
    • Disjuntor Recomendado: 25 A (Curva C)
    • Cabo CA: 4.0 mm²
  ```
##(O programa também gera automaticamente um arquivo Projeto_NomeDaCidade.png na pasta raiz com os gráficos)

🔮 Próximos Passos (Roadmap)
[ ] Interface Gráfica (GUI) com Streamlit ou CustomTkinter.

[ ] Geração automática de Proposta em PDF.

[ ] Módulo para Sistemas Híbridos e Off-Grid (Baterias).

[ ] Banco de dados local (SQLite) para histórico de clientes.

📄 Licença
Este projeto está sob a licença MIT. Sinta-se à vontade para contribuir!

Desenvolvido por: lebinho7


 
