![WhatsApp Image 2024-01-15 at 10 46 51](https://github.com/Wilkor/doc-plugin-fura-fila/assets/34819624/acaf6e2b-c51c-435d-ae54-becbc8fe0b47)

# Como utilizar a extensão Base64 to File!

Muito simples, basta seguir o passo a passo abaixo para ativar e configurar sua extensão:

- Ao lado de Home na tela principal, clique em Blip Store, depois no menu lateral, clique em extensões;
- Procure por **Base64 to File** e clique em ativar **(Instalar em seu bot Router/Roteador)**;
- Após a instalação da extensão, siga os passos abaixo;


# Como usar?

Depois de instalado a extensão, você terá a tela abaixo:

![image](https://github.com/Wilkor/doc-plugin-base64-to-file/assets/34819624/23d2c624-a2d3-4671-9461-f3b7dfb27749)


Agora, você deve selecionar o chatbot que você deseja copiar os blocos que serão responsáveis pela conversão da base64 para arquivo.

![image](https://github.com/Wilkor/doc-plugin-base64-to-file/assets/34819624/1b25d56e-a0ea-4884-9437-f8fa5b01d6c4)

Após clicar em instalar, você deve acessar o builder do chatbot selecionado, lá você terá 3 novos blocos, conforme tela abaixo:

![image](https://github.com/Wilkor/doc-plugin-base64-to-file/assets/34819624/b779d39c-b1c1-4b10-9bc8-d3fb21555878)




# Explicando cada bloco

Bloco -> **Converte base64 em PDF [ Convert base64 to PDF]**

Esse bloco é responsável por enviar duas informações para o servidor da .parse(), são elas:

- contact.identity = id do usuário;
- stringBase64 = variável que você tem que criar para receber a string base64 que vem de alguma consulta via API;
  
![image](https://github.com/Wilkor/doc-plugin-base64-to-file/assets/34819624/f12c7358-7f81-41fa-bd6f-2d8bc9ac3f78)

![image](https://github.com/Wilkor/doc-plugin-base64-to-file/assets/34819624/c6e27484-9db0-4c90-912c-66c46500eee4)

![image](https://github.com/Wilkor/doc-plugin-base64-to-file/assets/34819624/23a996b4-ca45-423e-884d-0efe5f231a40)

![image](https://github.com/Wilkor/doc-plugin-base64-to-file/assets/34819624/aeef55ee-de38-4c26-b2fa-4653413ef163)

![image](https://github.com/Wilkor/doc-plugin-base64-to-file/assets/34819624/2481508e-8245-4117-aa43-24452f75f939)


Bloco -> **Exibe arquivo [Display file]**

Esse bloco é responsável por exibir o arquivo depois de todo processo acima;

![image](https://github.com/Wilkor/doc-plugin-base64-to-file/assets/34819624/a5cc8037-f9f3-41df-878b-66dfdecefbc7)

![image](https://github.com/Wilkor/doc-plugin-base64-to-file/assets/34819624/144f484e-dc99-413f-ab7e-69beadc8a638)

![image](https://github.com/Wilkor/doc-plugin-base64-to-file/assets/34819624/86eb14a6-9fb5-49fe-9ca2-2ac3af185d7f)



Bloco -> **Retorno com erro [Return with error]**

Caso aconteça um erro nos dados enviados para o server (Bloco -> **Converte base64 em PDF [ Convert base64 to PDF]**), o cliente cairá no bloco abaixo.

![image](https://github.com/Wilkor/doc-plugin-base64-to-file/assets/34819624/e31d0d0f-9dcc-4e26-8f93-2ec6aa67dff8)

![image](https://github.com/Wilkor/doc-plugin-base64-to-file/assets/34819624/bea44b87-5e2b-4a4c-b1b0-e416dae01f92)

Existe uma frase padrão para o erro, mas você pode alterar da forma que precisar.


**Observação**: Antes de passar essa variável "stringBase64" para a chamada da extensão, faça uma condição de saída para verificar se a mesma contém um objeto com a seguinte propriedade: {'REDUCED':TRUE}, conforme tela abaixo:

![image](https://github.com/Wilkor/doc-plugin-base64-to-file/assets/34819624/3b51e99c-94bc-4694-89fe-e956bfe18c70)

Em caso positivo essa será redirecionada para o bloco de erro "Retorno com erro [Return with error]" ou outro bloco que você pode definir.

Isso acontece quando a stringBase64 é maior 49152 bytes.


Em caso de dúvidas, você pode entrar em contato conosco para tirar qualquer tipo de dúvida sobre a configuração da extensão

E-mail: contato@pontoparse.net
