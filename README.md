# geth.transparencia.me
Geth é um novo jeito de se comprar Ethereum. Após mais de um ano pesquisando uma maneira segura e transparente e não ter encontrado, resolvi criar essa solução.
* Vale lembrar que ela é destinada a iniciantes ou pessoas que querem manter o sigilo das transações, pois o custo da transação pelo paypal é alto e a solução acaba não sendo lucrativa para quem vende Ethereum
* Taxas do paypal: R$0,60 por transação + 5% de taxa do cartao de debito + 2,39% por parcela caso seja feita por cartão de crédito

> No momento, estou utilizando a conta do paypal da Trendt, que permite inclusive parcelar a compra e isso acarretaria num custo enorme

> O Afonso sugeriu que para uma próxima versão que o usuário compre em Reais e calculando o valor do ETH + taxas ele visualiza o tanto de ETHs que vai receber.

------
##### Passo a passo do front-end
1. Abrir uma conta de comerciante no paypal
2. Abrir uma conta no SendOwl (custo de +-15usd mês)
3. Criar um domínio (criei um subdomínio dentro do meu cpanel)
4. Instalar o Wordpress no domínio (eu instalei através do softaculous dentro do cpanel do servidor)
5. Criar os produtos dentro do SendOwl
6. Criar um novo artigo (possibilita que hajam comentários dos usuários), colar os códigos do botão no HTML
7. Instalar o plugin do Wordpress: MailChimp for WP
8. Criar conta no Mailchimp, exportar a API e colar no Mailchimp for WP
9. Criar uma lista personalizada no mailchimp (general form), inserir os fields desejados (utilizei além da carteira, o email, para poder cruzar com o paypal)
10. Na aba forms do Mailchimp for WP (dentro do wordpress), criei um formulário, e ele gerou um shortcode ```[mc4wp_form id="35"]```
11. Criei uma página nova chamada de ```done```, colei o shortcode
12. Volto no SendOwl, edito os produtos, inserindo a URL ```done``` que o usuário será redirecionado após a efetivação do pagamento

##### Passo a Passo back-end
1. No wordpress eu autorizei para que hajam comentários
