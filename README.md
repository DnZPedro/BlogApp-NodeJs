# BlogApp com Node.Js

Blog simples com login e cadastro de usuários e posts sobre tecnologia. A aplicação utiliza os pacotes: 

 - Express
 - Bcryptjs
 - Body-parser
 - Connect-flash
 - Express-handlebars
 - Express-session
 - Handlebars
 - Mongoose
 - Passport
 - Passport-local (Strategy)

## Config

Na pasta "**config**", temos um arquivo chamado **auth.js**, este arquivo utiliza do pacote "**passport**", que basicamente autentica o usuário. Ele busca o usuário no banco de dados, verifica se o usuário existe ou não e caso exista, verifica suas credenciais.  

## Helpers

A pasta "**helpers**" contém somente um arquivo, "**eAdmin.js**", quando criamos o modelo do usuário, um dos campos que o compõe é o "*eAdmin*", por padrão todos os usuários criados vem com esse campo sendo "**0**", ou seja, não é admin (*será melhor explicado mais pra frente*).

 >Resumidamente o eAdmin.js faz uma verificação no usuário para ver se ele é admin ou não, há páginas que somente quem é admin pode acessar.

## Models

É a pasta que contém os modelos que o MongoDB usa para criar suas coleções.  

Nesta pasta há 3 scripts: 

 - Categoria.js
   - É o model que cria as categorias das postagens. As categorias contém um nome, slug, e uma data de publicação.
 - Postagem.js
   - É o model que cria as postagens do blog. As postagens contém um título, slug, descrição, conteúdo, categoria e uma data de publicação.
 - Usuario.js
   - É o model que cria nossos usuários do blog. Os usuários contém um nome, email, aquela função eAdmin e uma senha.

## Public

Esta pasta contém todos os arquivos públicos da nossa aplicação.  

 >Nela contém os bootstraps usados na aplicação, tanto os scripts quando o css.

## Routes

Na pasta "**routes**", temos 2 tipos de rotas, uma exclusiva para o *admin* e outra para os *usuários* consumidores da aplicação. Não tem muito mistério, é somente as rotas que você acessaria normalmente em qualquer site.

 > Para acessar as páginas exclusivas do admin, somente sendo admin.

## Views


