# LAB--6-VLANs
Laboratório de 6 VLANs - Configuração e Troubleshooting

# Projeto 2 – Laboratório de VLANs e Roteamento

## 🔹 Objetivo
Configurar múltiplas VLANs, subinterfaces no roteador, e testar conectividade entre dispositivos. Desenvolver troubleshooting e documentação prática de rede.

---

## 🔹 Configurações das VLANs

| VLAN | Subinterface Roteador | Gateway IP       | Máscara      | Porta Switch Conectada |
|------|----------------------|-----------------|--------------|----------------------|
| 10   | G0/0.10              | 192.168.10.1    | 255.255.255.0| Fa0/1                |
| 20   | G0/0.20              | 192.168.10.33   | 255.255.255.0| Fa0/2                |
| 30   | G0/0.30              | 192.168.10.65   | 255.255.255.0| Fa0/3                |
| 40   | G0/0.40              | 192.168.10.97   | 255.255.255.0| Fa0/4                |
| 50   | G0/0.50              | 192.168.10.129  | 255.255.255.0| Fa0/5                |
| 60   | G0/0.60              | 192.168.10.161  | 255.255.255.0| Fa0/6                |

---

## 🔹 Configuração do Switch (trunks e acesso)

```text
interface Fa0/1
 switchport mode access
 switchport access vlan 10

interface Fa0/2
 switchport mode access
 switchport access vlan 20

interface Fa0/3
 switchport mode access
 switchport access vlan 30

interface Fa0/4
 switchport mode access
 switchport access vlan 40

interface Fa0/5
 switchport mode access
 switchport access vlan 50

interface Fa0/24
 switchport mode trunk
 switchport trunk allowed vlan 10,20,30,40,50,60


| Teste                          | Resultado        |
| ------------------------------ | ---------------  |
| Ping entre VLANs               | ✅ Sucesso      |
| Ping para gateway próprio VLAN | ✅ Sucesso      |
| Ping gateway outras VLANs      | ✅ Sucesso      |
| Troubleshooting de VLAN 60     | ⚠️ Ajuste trunk |
| VLAN 70 removida               | ✅ Confirmado   |


🔹 Troubleshooting
Problema identificado: VLAN 60 não estava passando pelo trunk da porta Fa0/4.
Solução: adicionado VLAN 60 ao allowed VLAN do trunk.
Observação: VLAN 70 removida por instabilidade de configuração.


🔹 Conclusão
Lab realizado com sucesso: 6 VLANs configuradas, gateways e subinterfaces corretos.
Todos os PCs testados com IPs estáticos e conectividade confirmada.
