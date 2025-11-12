# Como criar e publicar um repositório no GitHub — passos

1. Criar repositório no GitHub (web)
    - Aceder a https://github.com → New → escolher nome, visibilidade (Public/Private), opcionalmente adicionar README.

2. Configurar Git local (uma vez)

git config --global user.name "Seu Nome"
git config --global user.email "seu@email"

3. Criar o repositório local (novo projeto)

mkdir meu-projeto
cd meu-projeto
ni README.md
git init
git add .
git commit -m "Criei ficheiro"

4. Ligar o repositório local ao remoto (HTTPS)

git remote add origin https://github.com/USERNAME/REPO.git

5. Definir branch principal e enviar (push)

git push -u origin main ou master

6. Se o repositório remoto já tiver commits (por ex. README criado no site)

git pull --rebase origin main
# resolver conflitos se existirem
git push -u origin main

7. Verificar
    - Confirmar no GitHub que os ficheiros e commits aparecem.
    - Usar `git status`, `git log` localmente e `git remote -v` para verificar ligação.

Resumo mínimo de comandos (novo projeto):
```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/USERNAME/REPO.git
git branch -M main
git push -u origin main