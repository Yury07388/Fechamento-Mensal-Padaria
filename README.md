# Fechamento de Caixa

Controle diário de fechamento (dinheiro, cartão, Pix e saídas) com resumo mensal e anual.

- **Site:** servido pelo GitHub Pages a partir da branch `main`.
- **Dados:** ficam em `data.json` na branch `dados`, **criptografados** (AES-256-GCM, chave derivada do usuário + senha com PBKDF2). Sem a senha ninguém consegue ler — nem olhando o repositório.
- **Token do GitHub:** fica guardado dentro do arquivo criptografado; só é usado depois do login, para salvar.

## Primeiro acesso

1. Crie um token em <https://github.com/settings/personal-access-tokens/new>
   - *Repository access:* **Only select repositories** → este repositório
   - *Permissions → Repository → Contents:* **Read and write**
2. Abra o site e preencha a tela **Criar acesso** (usuário, senha e o token).
3. Para trazer os dados de janeiro/2026: **Opções → Importar backup…** e escolha o arquivo `janeiro-2026-backup.json` (que **não** deve ser enviado ao repositório).

## Observações

- Se esquecer a senha, os dados não podem ser recuperados. Faça backups em **Opções → Baixar backup**.
- Quando o token expirar, atualize em **Opções → Trocar senha / token**.
- O salvamento é automático alguns segundos após cada alteração.
