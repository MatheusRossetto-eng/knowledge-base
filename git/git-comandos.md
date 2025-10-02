# 📘 Guia Básico de Git

Este documento reúne os principais comandos do **Git** de forma prática e didática, para servir como referência rápida no dia a dia de desenvolvimento.

---

## ✍️ Autor

- **Matheus Rossetto**  
- Data: *01/10/2025*  

---

## 🚀 Comandos Essenciais

### 🔹 Inicialização
- `git init` → Cria um novo repositório Git local.

### 🔹 Clonando repositórios
- `git clone {url}` → Clona um repositório remoto na sua máquina.

### 🔹 Adicionando arquivos
- `git add {nome_do_arquivo}` → Adiciona um arquivo específico para a área de *stage*.  
- `git add .` → Adiciona todos os arquivos modificados para a área de *stage*.

### 🔹 Commitando alterações
- `git commit -m "{mensagem}"` → Salva as alterações no histórico do repositório.

### 🔹 Status e histórico
- `git status` → Mostra o estado atual do diretório e arquivos.  
- `git log --oneline` → Exibe o histórico de commits de forma resumida.

### 🔹 Sincronizando com o repositório remoto
- `git pull` → Baixa atualizações do repositório remoto.  
- `git push` → Envia as alterações para o repositório remoto.  
- `git remote -v` → Lista os repositórios remotos configurados.

### 🔹 Branches
- `git branch {nome_da_branch}` → Cria uma nova branch.  
- `git checkout {nome_da_branch}` → Troca para outra branch.  
- `git checkout -b {nome_da_branch}` → Cria e já troca para a nova branch.  
- `git merge (nome_da_branch}` → Mescla as alterações de outra branch na atual.

### 🔹 Comparando alterações
- `git diff` → Mostra as diferenças entre arquivos e o *stage area*.

### 🔹 Desfazendo alterações
- `git restore {nome_do_arquivo}` → Descarta alterações não adicionadas ao *stage*.  
- `git revert {commit_id}` → Desfaz um commit específico sem alterar o histórico.  
- `git reset {nome_do_arquivo}` → Remove um arquivo do *stage*.

---

## ⚡ Comandos Avançados

| Comando             | Função                                                                 |
|---------------------|------------------------------------------------------------------------|
| `git reset --soft`  | Desfaz o último commit, mas mantém as mudanças no *staging area*.      |
| `git reset --hard`  | ⚠️ CUIDADO! Descarta o último commit e todas as mudanças locais. Use apenas se tiver certeza. |
| `git stash`         | Salva temporariamente alterações não commitadas para trocar de branch rapidamente. |
| `git clean -fd`     | Remove arquivos não rastreados e diretórios vazios. Útil após testes de dependências temporárias. |

---

## 📌 Observações

- Sempre escreva mensagens de commit **claras e objetivas**.  
- Use branches para organizar funcionalidades, correções e experimentos.  
- Antes de dar `push`, execute `git pull` para evitar conflitos.  


📚 Este guia é parte do repositório de conhecimento sobre **Engenharia de Software** e pode ser expandido com dicas, boas práticas e fluxos de trabalho recomendados com Git.

