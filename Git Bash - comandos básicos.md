#  Git Bash - Comandos básicos



![](https://www.stanleyulili.com/assets/images/posts/2019-08-13-install-git-bash/featured-image.jpg)

Git é um sistema de versionamento de código comumente utilizado para projetos de desenvolvimento de software. Isso significa que ele trabalha como um intermediador entre um repositório local e um remoto (como por exemplo o GitHub), onde você pode controlar e administrar as alterações e atualizações do seu código. Lembrando que Git e GitHub não são a mesma coisa !!

Fica mais fácil de compreender o que é o Git quando analisamos o fluxo de trabalho do Git.

Se você estiver com pressa, aqui está um resumo dos comandos e o que fazem:



- **git init**: inicializa um repositório local git.
- **git status**: verifica o estado dos seus arquivos.
- **git add <nomeDoArquivo>**: envia seu arquivo especificado para o Stage.
- **git add - -all**: envia todos os arquivos para o Stage.
- **git commit -m “tituloDoCommit:** envia o que está no Stage para o HEAD.
- **git remote add origin urlDoRepositorio:** adiciona e indica a URL do repositório remoto em que os arquivos serão mantidos.
- **git push origin master:** envia os arquivos para o repositório remoto que você especificou através da URL do comando acima.
- **git checkout -b <nomeDaBranch>:** cria uma nova branch.
- **git checkout <nomeDaBranch>:** alterna para a branch especificada.



## Fluxo



De forma resumida, o Git abrange 3 camadas. O chamado “*Working Directory*”, que é onde você está codificando seu projeto, o “*Index*”, também chamado de “*Stage*”, que é uma camada onde você adiciona suas modificações de forma não permanente, ou seja, nesta camada você pode resetar as alterações que você incluiu no *Stage/Index* ou então partir para a próxima camada, a chamada de “*HEAD*”, quando você confirma suas alterações fazendo um “commit”. Porém essa ultima camada ainda não é o seu repositório remoto para o qual você deseja incrementar suas modificações. Para que o seu código chegue até o repositório remoto é necessario um comando muito simples chamado git push. Vou explicar melhor os comandos.



**Git Bash :**

Todo esse fluxo descrito acima é manipulado através do Git Bash (caso você utilize Windows). Contextualizando, o Git foi feito inicialmente para rodar em sistemas Unix, que não é o caso do Windows. Assim , foi criado o Git Bash, uma aplicação que emula um terminal Unix e permite que você desfrute dos comandos Git. O Git Bash já vem no pacote de instalação do Git para Windows.

**Comandos :**

Existem diversos comandos Git. Aqui eu vou demonstrar apenas alguns básicos porém suficientes para que você consiga criar seu repositório, e trabalhar de forma integrada com ele.

- Primeiro crie seu repositório seu local. Sua pasta onde ficará seu projeto.
- Entre na pasta e clique com o botão direito do mouse. Selecione o Git Bash:



![](https://miro.medium.com/max/1400/1*f_df_iyGHWkHG1pLphNZyw.png)



- Para iniciar o repositório utilize o comando **“git init”** :



![](https://miro.medium.com/max/1400/1*VMU9I0iQxwqHrOK7dA3iQA.png)



- Você pode verificar o status do repositório com o comando **“git status”**. É uma boa prática sempre conferir o status antes de iniciar com o fluxo das alterações e durante ele também :



![](https://miro.medium.com/max/1400/1*k7RW7_0INMuJQJdHj0lIlA.png)



Se você ainda não tiver nenhum arquivo nessa pasta, crie algum para continuar com o processo. Essa é a camada Working Directory.

- A próxima camada é o Index. Para mandar o seu arquivo para o index, basta utilizar o comando “**git add nomeDoArquivo**” ou se você quiser enviar ao Index todos os arquivos basta utilizar o parâmetro all. Assim: “**git add -all**” :



![](https://miro.medium.com/max/1400/1*f84yELNeiEwJ79M5sukS4g.png)



- Para verificar se o git está acompanhando seu arquivo, dê o comando “**git status**”. Se estiver tudo certo, aparecerá esta mensagem, o que significa que seu arquivo criado está na camada Stage :



![](https://miro.medium.com/max/1400/1*CNm2brYa6WQBtL4sSHR9eg.png)



- Depois que seus arquivos novos ou modificados estiverem na camada de Stage, você pode commita-los, ou seja, envia-los à ultima camada do fluxo, HEAD. Para isso use o comando “**git commit -m “tituloDoCommit”**. O parâmetro “-m” é passado para que você possa escrever uma descrição junto ao commit :



![](https://miro.medium.com/max/1400/1*6soweW-slnqL1ks2eHldkQ.png)



- Agora a última etapa do fluxo é enviar o(s) arquivo(s) ao repositório remoto. Se você ainda não tem, crie um repositório remoto, pode ser no GitHub, GitLab ou qualquer outro de sua preferência.

![](C:\Users\Leonardo David\Downloads\Screenshot_2.png)



- Depois de criado, copie a URL HTTP do seu repositório:



![](C:\Users\Leonardo David\Downloads\Screenshot_1.png)



- Volte ao Git Bash escreva o comando: “**git remote add origin urlDoRepositorio**”. Com esse comando você está especificando o repositório ao qual você deseja manter o seu projeto. “Origin” é apenas um apelido padrão, mas você pode utilizar qualquer nome :



![](https://miro.medium.com/max/1400/1*ajqeuwTDipGoO8ivlIUEbw.png)





- Depois de adicionado o repositório remoto, envie os arquivos utilizando o comando “**git push origin master**”.



![](https://miro.medium.com/max/1400/1*ssd7BcrNFPGNA5pnkjNQjw.png)





Master é o nome da branch padrão quando você cria um repositório, é onde ficará o seu código do produto final. Branch são ramificações do repositório, elas facilitam a organização do projeto, do time e garante segurança para o seu projeto final pois permitem que você trabalhe de forma isolada em diferentes funcionalidades e não tudo junto no produto final. Se você tiver outras branchs no seu repositório basta alterar o nome master para o nome da branch que você quer na hora do git push. Lembrando que antes de iniciar todo o fluxo, você ja deve estar na branch que deseja enviar suas alterações. Vou explicar melhor sobre Branches depois.

Processo finalizado. Após o git push seus novos arquivos ou novas alterações já estão no repositório, você pode ir até lá verificar.

**Branches**

Se você pretende desenvolver um projeto extenso ou então que abrange diferentes casos de uso, é recomendável que você separe seu projeto em branches. Você pode criar uma branch direto no seu repositório remoto, através da interface gráfica ou então através do Git Bash. Crie com o comando “**git checkout -b nomeDaBranch**”. O parâmetro “-b” significa git branch. Para navegar entre as branches utlize “**git checkout nomeDaBranch**”. Todo o processo descrito acima pode ser executado dentro das branches, conforme você for trabalhando nas diferentes funcionalidades do seu projeto.



![](https://miro.medium.com/max/1400/1*m9rRim4V04OvchtoMZOTPw.png)





Este é um fluxo básico de funcionamento do Git porém suficiente para que você consiga trabalhar integrado com um repositório remoto. Existem diversas outras possibilidades escondidas aí neste fluxo. É interessante dar uma lida na documentação do próprio Git e caso seja de interesse seu, aprofundar os estudos.