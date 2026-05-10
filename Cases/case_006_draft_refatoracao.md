# Playbook: Caso 006: Draft - Refatoracao

## 1. Metadados do Caso
* **ID do Caso:** CASE-006
* **Estado Inicial:** `Draft`
* **Tipo de Cenário:** `Refatoracao`
* **Responsável Principal:** Product Owner

## 2. Descrição do Cenário
Necessidade de revisão identificada em draft. Retornando para ajuste com comentário obrigatório.

## 3. Fluxo Esperado
```mermaid
graph TD
    A[Draft] -->|Ação: Revisão solicitada| B[Refatoracao]
```

## 4. Tratativa de Falhas (Estado Delayed)
Caso ocorra uma falha durante a transição para `Refatoracao`, o sistema entrará automaticamente no estado **Delayed**.

**Ações de Recuperação:**
1. **Retornar ao estado anterior:** Reverter para `Draft` e corrigir os dados de entrada.
2. **Avançar manualmente:** Forçar a transição para `Refatoracao` após resolução externa.
3. **Acionar Refatoração:** Enviar para revisão com comentário justificativo.

## 5. Sugestão de Evolução (Feedback Loop)
* **Para a Equipe Técnica:** Verificar logs de integração no n8n e garantir que os webhooks estão respondendo em tempo hábil.
* **Para o Cliente/Leigo:** Se o processo travar, verifique se todos os documentos necessários foram enviados corretamente. Nossa equipe será notificada automaticamente para ajudar.

---
*Gerado por Manus AI — Ecossistema API-First & API-AI-First*
