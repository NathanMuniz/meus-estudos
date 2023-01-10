## JSON Web Token

- JWT é um padrão que é usado para criar dados que podem conter assinatura, no qual podem ser validados, e pode conter dados encriptados, que podem ajudam na segurança da passagem de dados no formato JSON.
- JWT é um recurso para autorização, ou seja, ele é usado para autorizar um usuário autenticado a utilizar recurso que requer tal autorização.

(autorização vs autenticação) [anotacoes/autorizacao-autenticacao]

- Exemplo
    - O server providencia um Token, que diz que o usuário está logado como administrador para o client. O client então pode provar que ele é administrador usando esse token. O token recebe uma assinatura, normalmente do servidor, que pode ser certificado pela outra parte, o client.

- Estrutura
    - Header
        
        ```json
        {
        // Algoritimo usado para gerar a assinatura
          "alg": "HS256",	
          "typ": "JWT"
        
        }
        ```
        
    - Payload
        
        ```json
        {
          "loggedInAs": "admin",
          "iat": 1422779638
        }
        ```
        
        **************************************************************Campos com declarações padrões: 7 c**************************************************************ampos padrões que são comunmente incluendos em tokens. ex: (iat)
        
        ****************************************Campos customizados:**************************************** São incluindos dependendo do propósito do token.
        ex: (loggedInAs)
        
    - Assinatura
        
        Garante a validade dos token. 
        
        **********************Estrutura:********************** encoded header + “.” + encoded payload
        
    
    - Use
        - Diferente do abordagem tradicional, quando um usuário consegue logar com suas credenciais, ele Json Web Token, será retornado e devera ser salvo localmente, seja no local storage ou session storage.
