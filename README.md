# Plano de Ação — SMG1

Plataforma web para gestão de planos de ação da operação SMG1, hospedada no GitHub Pages.

## Como subir no GitHub

### 1. Criar o repositório

1. Acesse [github.com/new](https://github.com/new)
2. Escolha um nome (ex: `plano-de-acao-smg1`)
3. Marque **Private** (acesso restrito ao time)
4. Clique em **Create repository**

### 2. Subir os arquivos

Faça upload dos três arquivos deste pacote:
- `index.html` — o app
- `data.json` — os dados (começa vazio; o app popula)
- `README.md` — este arquivo

Via interface do GitHub:
1. Abra o repositório criado
2. Clique em **Add file → Upload files**
3. Arraste os três arquivos e faça commit

### 3. Ativar o GitHub Pages

1. No repositório, vá em **Settings → Pages**
2. Em **Source**, selecione `Deploy from a branch`
3. Branch: `main` | Pasta: `/ (root)`
4. Clique em **Save**

O site ficará disponível em:
`https://SEU-USUARIO.github.io/plano-de-acao-smg1`

---

## Controle de acesso

### Quem pode visualizar
- Repositório **Private**: apenas colaboradores convidados
- Repositório **Public**: qualquer pessoa com o link

### Quem pode adicionar/editar ações
Apenas colaboradores com **Write access** conseguem salvar alterações.

Para convidar:
1. **Settings → Collaborators → Add people**
2. Digite o usuário GitHub da pessoa
3. Escolha o nível: `Write` (pode editar) ou `Read` (só visualiza)

---

## Configurar o token no app

Para que o app consiga salvar no GitHub, cada usuário precisa configurar seu token:

1. Acesse o site do plano de ação
2. Clique em **⚙️ Config**
3. Preencha:
   - **Dono do repositório**: seu usuário ou organização GitHub
   - **Nome do repositório**: o nome que você escolheu
   - **Token**: gere em [github.com/settings/tokens](https://github.com/settings/tokens)
     - Tipo: Fine-grained token
     - Permissão: `Contents` → `Read and write`

O token fica salvo apenas no navegador local (localStorage) — não é compartilhado.

---

## Funcionalidades

- 5 abas (Plano de Ação, Plano de Guerra 2026, Compras, Report, Papéis e Responsabilidades)
- Busca e filtros por status, agenda e indicador
- Cards de resumo (total, feito, atrasado, em andamento, não iniciado)
- Adicionar, editar e excluir ações
- Ordenação por coluna
- Paginação (25 por página)
- Exportação CSV
- Sincronização automática com GitHub
