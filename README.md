# Automação de Envio de Mensagens via WhatsApp para Captação de Revendedores

## 📌 Visão Geral
Este projeto foi desenvolvido para **automatizar o envio de mensagens personalizadas via WhatsApp Web**, com foco na **captação de revendedores**. A solução foi pensada para ambientes corporativos **com fortes restrições técnicas**, onde **não é possível instalar Python, editores de código ou dependências no sistema**.

A automação utiliza **Python Portátil**, leitura de bases com **Pandas**, controle de sessão do WhatsApp Web e **logs detalhados**, garantindo rastreabilidade, facilidade de uso e confiabilidade operacional.

---

## 🎯 Objetivos do Projeto
- Automatizar o envio de mensagens personalizadas em escala
- Facilitar o uso por **usuários sem conhecimento técnico**
- Garantir controle, auditoria e rastreabilidade dos envios
- Operar em máquinas corporativas sem necessidade de instalação

---

## 🧠 Contexto de Negócio
Durante o projeto, foi essencial compreender:
- A **dinâmica entre stakeholders**, gestores e colaboradores
- As limitações técnicas impostas pelo ambiente corporativo
- A necessidade de uma solução **simples, segura e reutilizável**

O resultado foi uma ferramenta prática, intuitiva e alinhada aos objetivos comerciais.

---

## 🛠️ Tecnologias Utilizadas
- **Python Portátil (WinPython)**
- **pandas** – leitura e manipulação de bases com contatos
- **Selenium 4.8.3** – automação do navegador
- **Chromedriver / Chromium compatível**
- Base de automação: https://github.com/Kalebu/alright

Instalação da versão correta do Selenium:
```
pip install selenium==4.8.3
```

---

## 🌐 Compatibilidade de Navegadores (Ponto Crítico)
Um dos maiores desafios foi garantir compatibilidade entre:
- Versão do **Google Chrome / Chromium**
- Versão do **Chromedriver**

🔗 Link oficial para download das versões compatíveis:
https://googlechromelabs.github.io/chrome-for-testing/

⚠️ **Versões incompatíveis geram erros críticos na automação**.

---

## 🧩 Principais Desafios Técnicos
- ❌ Impossibilidade de instalar Python no sistema
- ❌ Ausência de editor de código
- ❌ Restrições de permissões administrativas
- ✅ Solução: uso de **Python Portátil totalmente isolado**

---

## 🖥️ Interface Intuitiva (CLI)
O sistema foi desenvolvido com uma **interface interativa no terminal**, permitindo:
- Escolha da sessão do WhatsApp
- Seleção da aba da planilha
- Definição de horário de envio

### Exemplo da Interface:
![Interface CLI](009.jpeg)

---

## 📊 Leitura da Base de Dados
- Base em planilha com **nomes e telefones**
- Leitura com **Pandas**
- Mensagens **personalizadas por contato**


---

## ⏱️ Humanização dos Envios
Para reduzir riscos de bloqueio:
- Delays aleatórios entre envios
- Envio em **blocos controlados (ex: 40 mensagens)**
- Simulação de comportamento humano com aleatoriedade nos delays

---

## 🧾 Logs e Auditoria (Ponto-Chave)
Cada envio gera um registro no arquivo `log_envio.txt`, contendo:
- Data e hora
- Nome do contato
- Número de telefone
- Status de envio

📌 Isso permite:
- Verificar se pedidos foram realmente executados
- Cruzar dados de pedidos com mensagens enviadas
- Garantir rastreabilidade operacional

### Exemplo de Log:
```
[28/01/2026 16:41:17] ENVIADO: Vinicius (1195*******)
[28/01/2026 16:41:32] ENVIADO: Joao (1198******)


## 🔄 Validação com Dados de Negócio
Após os envios:
- Exportação dos pedidos realizados
- Cruzamento com os logs
- Verificação se os números contatados efetivamente geraram pedidos

Essa etapa foi essencial para validar a efetividade da automação.

---

## 🚀 Resultado Final
- ✅ Solução funcional em ambiente restrito
- ✅ Fácil de usar por pessoas não técnicas
- ✅ Escalável e auditável
- ✅ Alinhada às necessidades do negócio

---

## 📁 Estrutura Sugerida do Repositório
```
📦 whatsapp-automation

 ┣ 📂 images
 
 ┃ ┣ terminal_interface.jpeg
 
 ┃ ┣ planilha_carregada.jpeg
 
 ┃ ┗ log_envio.jpeg
 
 ┣ send.py
 
 ┣ log_envio.txt
 
 ┣ README.md


## 👤 Autor
**Vinicius Mantovam**  
#Data Scientist #Automação #Análise de Dados #BI #Negócios

⭐ Se este projeto foi útil, sinta-se à vontade para deixar uma estrela no repositório!

