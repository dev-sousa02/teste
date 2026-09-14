Como subir trabalhos no Github: 
# 1. Entrar na pasta do projeto
cd "caminho/da/pasta"

# 2. Inicializar o repositório Git
git init

# 3. Renomear o branch padrão para "main"
git branch -M main

# 4. Adicionar os arquivos
git add .

# 5. Fazer o commit
git commit -m "Primeiro commit"

# 6. Conectar ao repositório do GitHub
git remote add origin https://github.com/seu-usuario/nome-repo.git

# 7. Enviar para o GitHub
git push -u origin main

Alterações:
git add .
git commit -m "descrição da alteração"
git push

Possíveis erros:
# Tentativa inicial de push (deu erro: "src refspec main does not match any")
git push -u origin main

# Verificando o que estava acontecendo
git status
# → mostrou "On branch master" (branch estava com nome errado)

# Renomeando o branch de "master" para "main"
git branch -M main

# Tentando o push novamente (deu erro: rejected, remote contains work you do not have)
git push -u origin main

# Trazendo o conteúdo do GitHub (README) para juntar com o projeto local
git pull origin main --allow-unrelated-histories

# Push final, agora com sucesso
git push -u origin main
