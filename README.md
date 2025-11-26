# Projeto-ASDF
Tutorial e Projeto Hello World c/ NodeJS e ASDF


1 - Faça a instalação do Oracle Virtual Box (VM)

2 - Faça a instalação do Ubuntu Desktop - https://ubuntu.com/download/desktop 

3 - Entre no seu VM e clique no local indicado 

<img width="1037" height="783" alt="image" src="https://github.com/user-attachments/assets/d88de3eb-6678-4bf1-8255-f93edfed0e80" />

4 - Colocar qualquer VM Name (Ex.: LinuxVM, UbuntuVM...)

5 - Escolher uma pasta para ficar localizado sua VM

6 - Jogar o arquivo baixado (Ubuntu) no espaço ISO IMAGE

7 - Apertar em próximo

<img width="778" height="418" alt="image" src="https://github.com/user-attachments/assets/29cabd0c-12fd-4288-b31b-6d72823aa242" />

8 - Esperar até que o Ubuntu abra e realizar tudo que se pede (Cadastro...) 

9 - Na tela inicial do Ubuntu dentro da Vm, clique com o botão direito na área de trabalho e abra o terminal

10 - Execute o primeiro comando: sudo apt update && sudo apt install git curl -y
 (Para instalar as ferramentas necessárias)

11 -Logo em seguida execute: git clone --branch v0.18.0 https://github.com/asdf-vm/asdf.git ~/.asdf
(Para clonar o repositório Github oficial do ASDF)  

------- CHECAR VERSÃO E FAZER UPDATE CASO NECESSÁRIO -------

1 - Execute o comando: asdf --version

A mensagem que deverá aparecer é essa:

<img width="459" height="48" alt="image" src="https://github.com/user-attachments/assets/4bd8fcdc-b619-4b1f-a647-2fb8c83c1940" />

Caso não apareça, faça: 

1 - Execute o comando nano ~/.bashrc

2 - Remova todas as linhas com “asdf.sh” e “completions/asdf.bash” do seu .bashrc

3 - Clique CTRL+O + ENTER (salvar) e depois CTRL+X (fechar) 

4 - Vá na pagina de releases do asdf - https://github.com/asdf-vm/asdf/releases

5 - Baixe o arquivo para Linux, por exemplo: asdf-v0.18.0-linux-amd64.tar.gz (1.5mb aprox.)

6 - Extraia o arquivo 

7 - Rode esses comandos no terminal:

- find ~/Downloads -name asdf
- mv /home/(nome do usuario)/Downloads/asdf-v0.18.0-linux-amd64/asdf ~/bin/
- chmod +x ~/bin/asdf
- ~/bin/asdf --version

______________________ CRIAR UM PROJETO OLA MUNDO COM NODEJS E ASDF ______________________

1 - Verifique se o asdf reconhece Node.js

asdf plugin list

2 - Se não aparecer nodejs, adicione:

asdf plugin add nodejs

3 - Instale uma versão do Node.js

asdf install nodejs 20.9.0

4 - No terminal, execute:

asdf set nodejs 20.9.0

5 - Depois você consegue rodar:

node --version
npm --version

6 - E então criar e rodar o projeto Node normalmente:

npm init -y

echo 'console.log("Olá, mundo!")' > index.js

node index.js

















