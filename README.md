# php-002-a-loja

##### Anotações OO:
1 - ...

##### Anotações Estruturado:
- Não é preciso colocar o "mysqli_close()" pq o PHP sabe se virar sozinho.
- Não fechar blocos PHP (?>) em arquivos só com PHP, evita de o usuário receber espaços em branco inseridos após o fechamento.
3 - Códigos mais importantes que o servidor devolve para o navegador:
    200 - tá tudo certo;
    404 - não achei (Page Not Found);
    500 - erro no servidor;
    302 - redireciona ae;
4 - Sempre use o "die()" após o redirecionamento com "header()" para evitar envio de dados criticos para o navegador.
6 - Não é uma boa ideia usar GET para adicionar e remover. Pq?
    6.1 - Limitação de caracteres na URI.
    6.2 - Plugins que aceleram a navegação, acessam escondido os links no corpo da pagina, para deixar em cache.
        <a href="remove-produto.php?id=12">Excluir</a>
    6.3 - GET significa "pegar dados" e não "mudar dados".
    6.4 - O GET não pode alterar o banco, senão o robo do Google acessa teu site, ae fu&*@.
7 - No PHP só duas strings são falsas:
    "0" e ""
    7.1 - O "false" é true.
8 - Quando um cookie é setado com tempo, ele expira somente depois de passado o tempo, mesmo se for fechado o browser.
9 - É possivel criar na mão o escopo de flash que são mensagens exibidas na proxima requisicao e deletadas da sessao.
10 - SQL injection:
    ' or id=1  or 'guilherme'='
11 - Diferença:
    11.1 - O "include" se não acha o arquivo gera uma WARNING.
    11.2 - O "require" se não acha o arquivo gera um ERROR.
    11.3 - O "require_once" inclui o arquivo uma vez so.