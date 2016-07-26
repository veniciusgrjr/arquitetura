# Pré-requisitos
  - Virtual Box
         ```
            $ sudo apt-get update
            $ sudo apt-get -y install virtualbox 
         ```
  - Vagrant
        ```
        $ sudo apt-get install vagrant
        ```
  - Install Git
        ```
           $ sudo apt-get install git-core
        ```
  - Configurar usuário Gti:
    ```
        $ git config --global user.name "Coloque seu nome de usuário aqui"
    ```
  - Configurar email
    ```
        $ git config --global user.email "seu_email@seu_provedor.com"
    ```
  - Clonar o repositório com o código para criar a arquitetura.
    ```
        $ git clone https://github.com/veniciusgrjr/arquitetura
    ```

  - Entrar no diretório.
    ```
        $ cd arquitetura
    ```

  - Baixar um box pré-configurado.
    ```
        $ vagrant box add hashicorp/precise32
    ```

  - Gerar toda a arquitetura.
    ```
        $ vagrant up
    ```

  - Ao final, teremos o site funcionando no endereço: http://192.168.33.12:8080/devopsnapratica/ 

