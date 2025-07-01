# 📊 Monitoramento de Máquinas Virtuais no Azure

## 📌 Descrição

Repositório criado como parte do desafio prático da DIO. O objetivo é aprender a configurar e gerenciar o **monitoramento de VMs no Azure**, garantindo visibilidade, controle e resposta proativa a eventos críticos, como exclusão de máquinas virtuais.

---

## 🎯 Objetivos

- Implantar o Azure Monitor Agent (AMA)
- Habilitar o VM Insights
- Criar Regras de Coleta de Dados (DCRs)
- Monitorar eventos críticos em VMs
- Documentar boas práticas e aprendizados

---

## 🔧 Ferramentas e Recursos

- **Azure Monitor**: coleta e análise de dados
- **VM Insights**: dashboard com métricas e mapas de dependência
- **Azure Monitor Agent (AMA)**: substitui agentes antigos; usa DCRs
- **DCR (Data Collection Rules)**: definem o que coletar, de onde e para onde
- **Log Analytics Workspace**: armazena logs e permite consultas KQL
- **Activity Log & Alertas**: visibilidade sobre ações como exclusão de VM

---

## 🚀 Passos para Configuração

1. **Instale o AMA** nas VMs (via portal, CLI, PowerShell ou políticas)
2. **Ative o VM Insights** para ver dashboards e métricas básicas
3. **Configure DCRs** para logs e métricas adicionais (Event Logs, Syslog, IIS, etc)
4. **Crie alertas personalizados** (ex: falta de heartbeat, uso de CPU, exclusão de VM)

---

## 📈 O que Monitorar

- **Métricas**: CPU, disco, rede, tempo de resposta
- **Logs**: Windows Event Logs, Syslog, IIS
- **Heartbeat**: verifique se a VM está respondendo
- **Eventos críticos**: exclusão de VM, falha no boot, uso excessivo de recursos

---

## ✅ Boas Práticas

- Use **AMA** + **DCRs** em vez de agentes legados
- Crie DCRs por grupos ou tipos de workload
- **Filtre** dados irrelevantes para reduzir custo
- **Evite duplicações** entre agentes/DCRs
- Automatize a implantação com **ARM, CLI ou Azure Policy**
- Monitore **heartbeat e disponibilidade** com alertas centralizados
