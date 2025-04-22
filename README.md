# 🚀 ServiceNow Lab - Scripts, Regras de Negócio e Automações

Bem-vindo ao meu laboratório de aprendizado com a plataforma **ServiceNow**! Aqui você encontrará exemplos práticos de scripts, business rules, integrações e outras funcionalidades criadas durante meus estudos e experimentações na plataforma.

## 📁 Estrutura

- `client-scripts/`: Exemplos de Client Scripts (onChange, onLoad, onSubmit).
- `business-rules/`: Regras de negócio para automação de processos.
- `script-includes/`: Funções reutilizáveis escritas em Script Include.
- `flows/`: Documentação de fluxos automatizados com Flow Designer.
- `ui-actions/`: Ações de UI como botões personalizados em formulários.

## 🧠 Objetivo

Este repositório tem como objetivo:

- Consolidar meus aprendizados com ServiceNow;
- Compartilhar exemplos úteis com outros profissionais;
- Criar um portfólio técnico que evolua com minha experiência na plataforma.

## 📌 Exemplos em destaque

### ✅ Validação com Client Script
```javascript
// Impede que o campo de prioridade seja "1 - Critical" se o impacto for "Low"
function onChange(control, oldValue, newValue, isLoading) {
    if (isLoading || newValue == '') return;

    var impact = g_form.getValue('impact');
    if (newValue == '1' && impact == '3') {
        g_form.showFieldMsg('priority', 'Prioridade crítica não é permitida para impacto baixo.', 'error');
        g_form.setValue('priority', '');
    }
}
```

## 📬 Contato

Se quiser trocar uma ideia ou colaborar com o repositório, me chama por aqui mesmo ou no https://www.linkedin.com/in/felipemichelettiferreira/

---

> Este repositório é um projeto pessoal e está em constante evolução à medida que avanço no estudo da plataforma ServiceNow.
