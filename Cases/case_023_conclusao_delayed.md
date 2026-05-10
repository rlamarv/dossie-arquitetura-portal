# Playbook: Caso 023: Conclusao - Delayed

## 1. Metadados do Caso
* **ID do Caso:** CASE-023
* **Estado Inicial:** `Conclusao`
* **Tipo de Cenário:** `Delayed`
* **Responsável Principal:** Gerente de Projeto

## 2. Descrição do Cenário
Recuperação de um estado Delayed em conclusao. O usuário optou por retornar ao estado anterior para corrigir dados.

## 3. Fluxo Esperado
```mermaid
graph TD
    A[Conclusao] -->|Ação: Recuperação manual| B[Conclusao]
```

## 4. Tratativa de Falhas (Estado Delayed)
Caso ocorra uma falha durante a transição para `Conclusao`, o sistema entrará automaticamente no estado **Delayed**.

**Ações de Recuperação:**
1. **Retornar ao estado anterior:** Reverter para `Conclusao` e corrigir os dados de entrada.
2. **Avançar manualmente:** Forçar a transição para `Conclusao` após resolução externa.
3. **Acionar Refatoração:** Enviar para revisão com comentário justificativo.

## 5. Sugestão de Evolução (Feedback Loop)
* **Para a Equipe Técnica:** Verificar logs de integração no n8n e garantir que os webhooks estão respondendo em tempo hábil.
* **Para o Cliente/Leigo:** Se o processo travar, verifique se todos os documentos necessários foram enviados corretamente. Nossa equipe será notificada automaticamente para ajudar.

---
*Gerado por Manus AI — Ecossistema API-First & API-AI-First*
