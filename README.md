# 🔐 Segurança da Informação & Criptografia Prática com GPG (`Criptografia_GPG`)

![Security](https://img.shields.io/badge/Cybersecurity-Criptografia-E11D48?style=for-the-badge&logo=gnuprivacyguard&logoColor=white)
![Linux](https://img.shields.io/badge/GnuPG-RSA_2048_%2F_4096-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![License](https://img.shields.io/badge/License-MIT-emerald?style=for-the-badge)

Repositório dedicado às aulas práticas da disciplina **Conceitos de Segurança da Informação**, abordando desde os pilares fundamentais (**Confidencialidade, Integridade e Disponibilidade — CID**) até práticas avançadas de criptografia assimétrica e proteção de dados.

---

## 📚 Tópicos Abordados

- **Criptografia Assimétrica (RSA):** Geração de pares de chaves pública/privada (`2048 bits` e `4096 bits`) para troca segura de arquivos e autenticação.
- **PGP (Pretty Good Privacy) & GnuPG (GPG):** Assinatura digital, criptografia e descriptografia de documentos e mensagens.
- **Criptografia de Disco e Volumes:**
  - 🪟 **BitLocker (Windows):** Proteção de volumes inteiros no sistema operacional da Microsoft.
  - 🍎 **FileVault & VeraCrypt (macOS / Multiplataforma):** Criptografia de discos e containers seguros.
  - 🐧 **LUKS (`Linux Unified Key Setup`):** Padrão de criptografia de partições no Linux integrado ao `dm-crypt`.

---

## 💻 Guia Rápido de Comandos GPG (Laboratório Prático)

### 1. Gerar um novo par de chaves (Pública e Privada)
```bash
gpg --full-generate-key
```

### 2. Listar chaves públicas instaladas no chaveiro
```bash
gpg --list-keys
```

### 3. Exportar sua chave pública para compartilhar
```bash
gpg --armor --export seu_email@dominio.com > chave_publica.asc
```

### 4. Importar a chave pública de um destinatário
```bash
gpg --import chave_do_professor.asc
```

### 5. Criptografar um arquivo (`.docx`, `.pdf`, `.txt`) para um destinatário
```bash
gpg --encrypt --recipient destinatario@dominio.com Trabalho_Criptografia.docx
# Gera o arquivo criptografado: Trabalho_Criptografia.docx.gpg
```

### 6. Descriptografar um arquivo `.gpg` recebido
```bash
gpg --output Trabalho_Descriptografado.docx --decrypt Trabalho_Criptografia.docx.gpg
```

---

## 👨‍🏫 Professor Responsável

**Mizael Souto** (`@mizaelsouto`) — [LinkedIn](https://www.linkedin.com/in/mizaelsouto)  
Distribuído sob a licença **MIT** ([LICENSE](./LICENSE)).
