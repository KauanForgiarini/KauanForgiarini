# Kauan Forgiarini

O fio condutor dos meus projetos é sempre a mesma pergunta: **como transformar leitura de sensor em decisão automática confiável?** Apliquei isso primeiro à irrigação de soja e, mais recentemente, à detecção de ataques em estações terrestres de satélite.

Ciência da Computação (UFSM) e Inteligência Artificial (FIAP), ambos no 2º semestre · Comercial & Dev Web na [CompactJr](https://github.com/CompactJr) · Santa Maria, RS

---

### 🛰️ [orbit-shield](https://github.com/KauanForgiarini/orbit-shield) — detecção de intrusão em ground stations satelitais

Em fevereiro de 2022, um cyberataque contra a rede de satélites ViaSat KA-SAT derrubou comunicações militares e civis na Europa horas antes da invasão da Ucrânia — o vetor foi a estação terrestre. O ORBIT-SHIELD é uma prova de conceito de defesa em 5 camadas para esse mesmo tipo de infraestrutura: firmware ESP32 assinando telemetria com HMAC-SHA256, API em FastAPI com rate limiting e validação anti-replay, PostgreSQL com audit log imutável, e duas camadas de Machine Learning — Isolation Forest para anomalias (**recall de 93,4%**) e Random Forest para classificação (**96,9% de acurácia**). A modelagem de ameaças segue o framework **STRIDE**, com 8 ameaças mapeadas a contramedidas específicas.

### 🌱 FarmTech — de irrigação automática a pipeline de regressão

Comecei simulando um ESP32 no Wokwi que decide sozinho quando irrigar soja, cruzando umidade do solo, pH, nutrientes e previsão de chuva via API. Evoluí a solução em duas frentes: um [dashboard com banco Oracle e 5 modelos de classificação](https://github.com/KauanForgiarini/farmtech-crop-monitor) para recomendação de cultura (Random Forest chegou a **~99% de acurácia**), e um [pipeline de regressão](https://github.com/KauanForgiarini/farmtech-data-pipeline) que prevê volume de irrigação, fertilização e rendimento de safra — Gradient Boosting explicou **81% da variância** no volume de irrigação, superando Regressão Linear e Ridge. Um motor de decisão em C++ traduz essas previsões em recomendações de manejo.

→ [Firmware e lógica de decisão original (Fase 2)](https://github.com/KauanForgiarini/FarmTech)

<details>
<summary><strong>Outros projetos</strong></summary>
<br>

**[AgroSafe](https://github.com/KauanForgiarini/AgroSafe)** — sistema em terminal para registrar e classificar perdas na colheita de soja, com recomendações baseadas em parâmetros da EMBRAPA.

</details>

---

**Stack:** Python · C/C++ · R · SQL (Oracle, PostgreSQL) · FastAPI · Streamlit · Scikit-learn · ESP32

🔭 Agora aprofundando lógica de programação, com JavaScript, CSS e Node como próximos passos.

[LinkedIn](https://www.linkedin.com/in/kauanforgiarini) · [kauanforgiarini@gmail.com](mailto:kauanforgiarini@gmail.com)
