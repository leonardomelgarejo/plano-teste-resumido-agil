# Plano de Testes Resumido - Contexto Ágil

## 1. Objetivo dos Testes

Validar a funcionalidade de login, garantindo autenticação com dados válidos e tratamento de erros com dados inválidos.

---

## 2. Escopo dos Testes

### Escopo Incluído:
- Login de usuário
- Cadastro de novo usuário
- Recuperação de senha

### Fora do Escopo:
- Testes de performance
- Testes de segurança
- Integração com serviços de terceiros

---

## 3. Tipos de Testes
- Testes funcionais de API (Postman / REST Assured)
- Testes de interface web (Selenium / Playwright)
- Testes exploratórios manuais
- Testes unitários (devs)

---

## 4. Critérios de Aceitação / Pronto para Testar
- Histórias com critérios de aceitação revisados pelo PO
- Feature desenvolvida e mergeada na branch `develop`
- Build de CI executado com sucesso
- Ambiente de QA disponível

---

## 5. Critérios de Saída / Pronto para Entrega
- Testes manuais e automatizados concluídos
- Nenhum defeito de severidade Alta/Crítica em aberto
- Validação da história pelo PO em homologação
- Relatório de testes atualizado no Jira ou Allure

---

## 6. Responsabilidades
| Papel   | Atividade                                 |
|---------|-------------------------------------------|
| QA      | Testes manuais e execução de automações   |
| Dev     | Testes unitários e correção de bugs       |
| PO      | Validação de critérios de aceite          |

---

## 7. Ferramentas
- **Jira** – Gestão de tarefas e bugs  
- **GitHub Actions** – Pipeline de CI/CD  
- **Allure** – Relatórios de testes  
- **Postman / REST Assured** – Testes de API  
- **Selenium / Playwright** – Testes de UI  

---

## 8. Riscos e Mitigações
| Risco                                  | Mitigação                                         |
|----------------------------------------|---------------------------------------------------|
| API instável em QA                     | Uso de mocks com WireMock                        |
| Ambiente de homologação fora do ar     | Plano B com ambiente local                       |

---

## 9. 🔄 Status de Execução dos Testes

| ID da História | Funcionalidade             | Tipo de Teste     | Status       | QA Responsável | Observações                     |
|----------------|----------------------------|-------------------|--------------|----------------|---------------------------------|
| US-101         | Login com usuário válido   | Manual / Automat. | ✅ Passou     | Juliana        | Validado em QA                 |
| US-102         | Recuperação de senha       | Manual            | 🚧 Em teste   | Leonardo       | Falha no envio de e-mail       |
| US-103         | Cadastro de novo usuário   | Automatizado      | ❌ Falhou     | Juliana        | Bug #321 aberto no Jira        |
| US-104         | Validação de campos obrig. | Manual            | ⏳ Aguardando | Leonardo       | Aguardando deploy da feature   |
