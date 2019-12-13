# Guia de Contribuição (Contributing Guide)
## Português brasileiro
Muito obrigada por reservar uma parte do seu tempo para contribuir com o nosso projeto! :heart_eyes:
Esse é um pequeno guia para ajudar na sua contribuição. Se julgar necessário, você pode até sugerir mudanças por aqui também! Para começar, aqui está uma pequena lista com alguns links úteis:
* [Código de Conduta do Meninas Digitais](https://github.com/meninasdigitaispiaui/codigo-de-conduta)
* [Um tutorial geral de git, caso você queira fazer mais coisas com essas informações](https://rogerdudler.github.io/git-guide/index.pt_BR.html)

### Como contribuir
Você deve, respectivamente:
1. Forke o repositório
2. Clone o repositório forkado no seu computador
3. Faça as alterações que julgar necessárias e mande a Pull Request!

#### Forkando o repositório
No lado direito superior da tela, quando você acessa o repositório do projeto, você verá 3 botões: Watch, Star e Fork. Clique em Fork e, se aparecer uma tela perguntando "Where should we fork this repository?" (Onde devemos forkar esse repositório?), escolha seu nome de usuário. Pronto, agora você tem uma cópia do repositório no seu perfil!

#### Clonando localmente
Separamos tutoriais interessantes sobre essa etapa, de acordo com o seu sistema operacional:
* [Mac](https://help.github.com/pt/github/creating-cloning-and-archiving-repositories/cloning-a-repository)
* [Windows](http://gabsferreira.com/forkando-e-clonando-um-repositorio-no-github/)
* [Linux](https://help.github.com/pt/github/creating-cloning-and-archiving-repositories/cloning-a-repository)

Mas, em resumo, você:
1. Abrirá um terminal
2. Executará alguns comandos:
	* Se você está iniciando, por exemplo, crie uma pasta chamada Github para guardar seus repositórios clonados com `mkdir Github`
	* Se você já tem algo parecido com essa pasta, direcione-se para ela com o comando `cd Github`
	* Use `git clone https://github.com/ + SEU NOME DE USUÁRIO + /meninasdigitaispiaui.github.io.git` para clonar o repositório nessa pasta, e depois `cd meninasdigitaispiaui.github.io` para direcionar-se para a pasta do repositório clonado
3. Poderá alterar os arquivos	

#### Alterando os arquivos
Aqui, você poderá:
	* Adicionar arquivos
	* Implementar alterações em textos
	* Alterar outros arquivos já existentes
	* Corrigir bugs
	* Entre outros
Obviamente, na sua pasta local. Não esqueça de atualizar o status antes de quaisquer alterações com métodos como o `git fetch --all` e `git rebase origin master`, e verificá-lo usando `git status`.
Ah, o principal - não esqueça de comitar suas alterações usando `git commit -m "Ação"`. É uma boa prática usar um verbo no presente e outras palavras em minúsculo para o nome da ação, como "Add contributing guide" ou "Adiciona guia de contribuição".

#### Mande a pull request!
Ao terminar suas alterações, dê um `git push origin master` para que as alterações sejam enviadas ao GitHub. No repositório original, aparecerá uma mensagem sugerindo um pull request. Pode enviar!

### Contribua para esse guia!
As contribuições direcionadas especificamente a esse guia também são incentivadas! Mande seu PR que a gente revisa rapidinho!