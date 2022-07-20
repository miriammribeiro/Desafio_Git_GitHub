1. Passos para criar chave ssh:

   - no Git Bash : **$ ssh-keygen -t <nome da chave> -C <email>** (serão criadas as chaves pública e privada na pasta .ssh)
   - Para adicionar a chave no GitHub é preciso executar o comando **cat** da chave pública que se encontra na pasta .ssh e incluí-la na  no settings / profile/ ssh keys da conta do GitHub.
   - Após colocar a chave no GitHub, inicializá-la no Git Bash (start do ssh agent) em background: **$ eval $(ssh-agent -s)**
   - Adicionar no Agent a chave privada: **$ ssh-add <chave privada>**



2. Configuração de Token no GitHub:

- Em Developer Settings / Personal Access Tokens:
  - dar um nome para o Token (note)
  - colocar um período para expiração do token
  - clicar em repo
  - generate token



3. Comandos no Git:

- Iniciar o Git : **git init**
- Iniciar o versionamento: **git add * / git add. / git add <nomearq>**
- Criar um commit: **git commit -m "<texto>"**
- Configurações no Git (geralmente configurações iniciais). Pode ser global ou apenas no repositório:  **git config --global user.email <email>**
- Verificar o status: **git status**
- Lista configurações do GitHub: **git config --list**
- Remover uma configuração (unset): **git config --global --unset user.email**



4. Configuração GitHub / Git Bash:

- adicionar a origem: **git remote add origin <url do repositório obtida no GitHub>**
- lista de remotes que tem cadastrado: **git remote -v**
- levar repositório local para o repositório remoto: **git push origin master**
- atualizar repositório do GitHub para o Git Bash: **git pull origin master**
- baixar código do GitHub para o Git Bash: **git clone <url do repositório obtida no GitHub>**