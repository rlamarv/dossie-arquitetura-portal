# Playbook: Caso 045: Oportunidade - Falha

## 1. Metadados do Caso
* **ID do Caso:** CASE-045
* **Estado Inicial:** `Oportunidade`
* **Tipo de Cenário:** `Falha`
* **Responsável Principal:** Comercial

## 2. Descrição do Cenário
Falha ao tentar avançar a partir de oportunidade. O sistema entrou em estado Delayed para proteção.

## 3. Fluxo Esperado
```mermaid
graph TD
    A[Oportunidade] -->|Ação: Erro de sistema / Timeout| B[Delayed]
```

## 4. Tratativa de Falhas (Estado Delayed)
Caso ocorra uma falha durante a transição para `Delayed`, o sistema entrará automaticamente no estado **Delayed**.

**Ações de Recuperação:**
1. **Retornar ao estado anterior:** Reverter para `Oportunidade` e corrigir os dados de entrada.
2. **Avançar manualmente:** Forçar a transição para `Delayed` após resolução externa.
3. **Acionar Refatoração:** Enviar para revisão com comentário justificativo.

## 5. Sugestão de Evolução (Feedback Loop)
* **Para a Equipe Técnica:** Verificar logs de integração no n8n e garantir que os webhooks estão respondendo em tempo hábil.
* **Para o Cliente/Leigo:** Se o processo travar, verifique se todos os documentos necessários foram enviados corretamente. Nossa equipe será notificada automaticamente para ajudar.

---
*Gerado por Manus AI — Ecossistema API-First & API-AI-First*
