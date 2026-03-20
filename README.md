# 🚀 SSH Shield

> 🔐 Monitoramento de tentativas de login SSH em uma instância na nuvem

---

## 🧠 Visão Geral

O **SSH Shield** é um projeto prático focado em segurança básica de servidores Linux na nuvem.

A proposta é monitorar tentativas de login via SSH em uma instância, identificando acessos inválidos e exibindo os IPs envolvidos.

Esse projeto foi desenvolvido como laboratório para prática de:
- Cloud (infraestrutura básica)
- Linux
- Segurança

---

## ⚙️ Tecnologias Utilizadas

- 🐍 Python → análise de logs  
- 🖥️ Amazon EC2 → execução do servidor  
- 🌐 VPC → configuração de rede da instância  
- 🔐 SSH → acesso remoto  

---

## 🏗️ Como Funciona

1. A instância é criada dentro de uma VPC  
2. O acesso SSH é habilitado  
3. Tentativas de login são registradas no sistema (`/var/log/auth.log`)  
4. Um script em Python analisa esses logs  
5. O sistema identifica:
   - Quantidade de tentativas falhas  
   - IPs envolvidos  

---

## 📸 Demonstração

### 🔹 Criação da VPC
Configuração da rede onde a instância foi provisionada.

### 🔹 Instância em execução
Servidor rodando na EC2 com acesso SSH habilitado.

### 🔹 Conexão SSH
Acesso remoto realizado via PuTTY.

### 🔹 Script de monitoramento
Código em Python responsável por analisar falhas de login.

---

## 💡 Desafios Enfrentados

- 🔐 Permissão para acessar arquivos de log do sistema  
- 🔎 Ajuste da expressão regular para capturar os IPs corretamente  
- 🌐 Configuração inicial da VPC e acesso externo  
- 🔌 Primeira conexão SSH via PuTTY  

---

## 📈 Resultados

- ✅ Monitoramento funcional de tentativas de login SSH  
- ✅ Identificação de IPs suspeitos  
- ✅ Execução prática em ambiente real na nuvem  

---

## 🎯 Aprendizados

- Fundamentos de rede (VPC)  
- Criação e acesso a servidores na nuvem  
- Leitura e análise de logs Linux  
- Uso de Python para automação simples  

---

## ▶️ Como Executar

```bash
# Conectar na instância
ssh ec2-user@<IP>

# Executar o script
python3 monitor_ssh.py
