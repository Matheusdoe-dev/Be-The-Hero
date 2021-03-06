<h1>Minhas anotações - Semana Omnistack 11</h1>

<h2>Dia 1 - Conhecendo a Omnistack</h2>

<h3>Back End e Front End</h3>

<h4>Back End</h4>

<p>Os bastidores da aplicação. A parte que o usuário não visualiza. É onde fica:</p>
<ul>
    <li>Regras de negócio;</li>
    <li>Conexão banco de dados;</li>
    <li>Envio de e-mail;</li>
    <li>Comunicação com webservices;</li>
    <li>Autentificação do usuário;</li>
    <li>Criptografia e segurança;</li>
</ul>

<!-- <img src="img/img-2.png" alt="Arquitetura da aplicação"> -->

<h4>JSON</h4>

<ul>
    <li><em>JavaScript Object Notation</em></li>
    <li>Uma linguagem , "idioma", usada para fazer o meio campo, a comunicação entre o Back End
        e o Front End
    </li>
    <li>É uma estrutura de dados.</li>
</ul>

<h3>Entendendo o React</h3>

<h4>Abordagem tradicional</h4>
<ul>
    <li>Na abordagem tradicional, a cada requisição, o servidor retorna o conteúdo
        completo da página, contendo todo HTML e CSS.
    </li>
    <li>Essa abordagem limita o front-end para o browser já que o aplicativo mobile ou
        serviços externos não vão conseguir interpretar o HTML.
    </li>
</ul>
<img src="img/img-3.png" alt="">

<h4>Abordagem de SPA</h4>
<ul>
    <li>Na abordagem de SPA (<em>Single Page Application</em>), as requisições trazem apenas
        dados como respostas e, com esses dados, o front-end pode preencher as informações
        em tela.
    <li>A página nunca recarrega, otimizando a performance e dando vida ao conceito de SPA.
        Retornando apenas JSON podemos ter quantos front-ends quisermos.
    </li>
</ul>
<img src="img/img-4.png" alt="">

<h3>Entendendo o React Native</h3>

<h4>Abordagem tradicional</h4>
<ul>
    <li>Na abordagem tradicional, criamos uma aplicação para iOS e outra para Android, e nesses casos, o trabalho se torna repetido tanto para criação quanto para as alterações no projeto.
    </li>
</ul>
<img src="img/img-5.png" alt="">

<h4>Abordagem do React Native</h4>
<ul>
    <li>Todo código feito é em <strong,>JavaScript</script>, esse código <strong>não é 
        convertido em código nativo, melhor do que isso, o dispositivo passa a entender o código JavaScript
        e a interface gerada é totalmente nativa
    </strong>
    </li>
</ul>
<img src="img/img-6.png" alt="">

<h4>JavaScript core</h4>
<ul>
    <li>
        O <em>JavaScript core</em> é implementado pelo React Native dentro da nossa aplicação
        iOS/Android. Ele é um framework que dá o entendimento da linguagem JavaScript para o
        sistema operacional mobile.
    </li>
</ul>

<h3>Por que utilizaremos o Expo</h3>
<img style="width: 600px;" src="img/img-7.png" alt="">

<ul>
    <li>
        É um "framework", um conjunto de ferramentas/bibliotecas pronta para se utilizar a grande
        maioria de funcionalidades do mobile (camera,mapa,sensores,etc).
    </li>
    <li>
        Sem o Expo, precisamos instalar em nosso sistema tanto o Android Studio para obter a
        SDK de desenvolvimento Android, e o Xcode (apenas no Mac) para obter a SDK do iOS.
    </li>
    <li>
        Nesse caso, nossa iniciação no desenvolvimento fica mais penosa, já que essas SDK's 
        não são extremamente simples de instalar e livres de erros
    </li>
    <li><strong>SDK -></strong><em>Software Development Kit</em></li>
</ul>

<h4>Arquitetura do Expo</h4>
<img src="img/img-8.png" alt="">

<ul>
    <li>Com o Expo, nós instalamos um aplicativo no celular chamado Expo, e dentro dele, tudo
        o que precisamos para desenvolver no React Native já está instalado, como as API's de
        mapas, geolocalização, câmera, sensores, calendário, etc...
    </li>
    <li>
        Com isso, não precisamos nos preocupar em gerar o aplicativo pra Android e iOS já que
        o app do Expo instalado tem tudo o que precisamos e assim usamos apenas React.
    </li>
</ul>

<hr>

<h2>Dia 2 - Criado a base da aplicação</h2>

<h3>Metodos HTTP</h3>

<ul>
    <li><strong>GET:</strong>Utilizado quando se quer <em>buscar/listar</em> uma informação.</li>
    <li><strong>POST:</strong>Utilizado quando se quer <em>criar</em> uma informação no backend</li>
    <li><strong>PUT:</strong>Utilizado quando se quer <em>alterar</em> uma informação no backend</li>
    <li><strong>DELETE:</strong>Utilizado quando se quer <em>deletar</em> uma informação no backend</li>
</ul>

<h3>Insomnia</h3>

<ul>
    <li>Software utilizado para testar rotas.</li>
</ul>

<h3>Routes</h3>

<h4>app.post('/users', (<strong>request</strong>, response)</h4>
<ul>
    <li>
        O <strong>request</strong> guarda todos os dados que vem através de uma requisição.
    </li>
</ul>

<h4>app.post('/users', (request, <strong>response</strong>)</h4>
<ul>
    <li>
        O <strong>response</strong> é o responsavel por retornar uma resposta ao usuário.
    </li>
</ul>

<h3>Tipos de Parametros</h3>

<h4>Query params</h4>
<ul>
    <li>Parametros enviados dentro da URL.</li>
    <li>Parametros nomeados enviados na rota após o '?'</li>
    <li>Geralmente servem para filtros, paginação</li>
    <li><em>'/users?name:Diego'</em> ou <em>'/users?name:Diego&idade=25'</em></li>
</ul>

<h4>Route params</h4>
<ul>
    <li>Parametros utilizados para identificar recursos.</li>
    <li>Identificar um único recurso. Ex.: Um único usuario.</li>
    <li><em>'/users/:id'</em></li>
</ul>

<h4>Request Body</h4>
<ul>
    <li>Corpo da requisição utilizado para criar ou alterar recursos</li>
</ul>

<h4>Request Headers</h4>
<ul>
    <li>Cabeçalho da requisição</li>
    <li>Geralmente onde fica informação do contexto da requisição.</li>
    <li>É onde geralmente fica dados da autenticação do usuario, localização, etc.</li>
</ul>

<h3>Banco de Dados</h3>

<h4>Diferenças entre bancos de dados</h4>

<h5>Banco de Dados hoje no mercado</h5>

<ul>
    <li>SQL: MySQL, SQLite, PostgreSQL, Oracle, Microsoft SQL Server</li>
    <li>NoSQL: MongoDB, CouchDB, etc</li>
</ul>

<h5>SQL</h5>
<ul>
    <li>É o mais utilizado atualmente no mercado.</li>
    <li>Permite ter um controle maior da estrutura.</li>
</ul>

<h5>NoSQL</h5>
<ul>
    <li>Bancos não relacionais</li>
    <li>Os Schemas da tabela, a estrutura da tabela, os campos que ela vai armazenar
        , fica muito livre e pouco estruturado.
    </li>
</ul>

<h4>Migrations</h4>
<ul>
    <li>Funcionalidade do knex para criar tabelas, manter um histórico das tabelas que foram
        criadas e alteradas.
    </li>
    <li>Como se fosse um controle de versões do banco de dados.</li>
</ul>

<h3>CORS</h3>

<ul>
    <li>Modulo de segurança</li>
    <li>Modulo que vai determinar quem vai poder acessar a aplicação.</li>
</ul>

<hr>

<h2>Dia 3 - Construindo a interface web</h2>

<h3>Conceitos de React</h3>

<h4>Componentes</h4>
<ul>
    <li>Componentes no React são funções JavaScript que retornam HTML</li>
    <li>Componentes permitem você dividir a UI em partes independentes, 
        reutilizáveis e pensar em cada parte isoladamente.</li>
    <li>Um componente React válido aceita um único argumento de objeto <strong>"props"</strong></li>
    <li>São chamados de <strong>Componentes de função</strong> porque são literalmente
    funções JavaScript</li>
</ul>

<h4>JSX</h4>
<ul>
    <li><em>JavaScript XML</em></li>
    <li>HTML escrito dentro do JavaScript</li>
</ul>

<h4>Estado</h4>
<ul>
    <li>Uma informação que vai ser mantida pelo componente.</li>
    <li>No React, não se pode usar simplesmente variaveis convensionais para manipular
        dados nos componentes.
    </li>
    <li><strong>Imutabilidade :</strong>Dentro do React, por questões de performance, não se pode
    manipular a variavel do estado, ou seja, o estado diretamente. Tende <em>sobrepor</em>.</li>
</ul>

<h5>Metodo useState()</h5>
<ul>
    <li>Quando esse metodo é utilizado, ele retorna um array com duas posições.</li>
    <li><strong>[valor, funcaoDeAtualizacao]</strong> A primeira posição é a variavel, a segunda
    é a função de atualização</li>
</ul>

<h3>React Router Dom</h3>
<ul>
    <li>
        <strong>react-router-dom</strong>: Pacote utilziado para lidar com rotas na aplicação.
    </li>
    <li>
        <strong>BrowserRouter</strong>: Precisa ficar em volta das rotas para que o roteamento
        funcione.
    </li>
    <li>
        <strong>Switch</strong>: Tem a função de garantir que apenas uma rota seja executada por
        momento
    </li>
</ul>

<h3>useEffect</h3>
<ul>
    <li>
        Serve para disparar alguma função em um determinado momento do componente.
    </li>
</ul>

<hr>

<h2>Dia 4 - Construindo a interface mobile</h2>

<hr>

<h2>Dia 5 - Adicionando funcionalidades avançadas</h2>

<h3>Validação</h3>

<h4>Celebrate & Joi</h4>
<ul>
    <li>Utilizado para fazer validação de entrada de informação nas rotas.</li>
</ul>

<h3>Testes</h3>

<ul>
    <li><strong>TDD</strong>: <em>Test-Driven Development</em> ou Desenvolvimento dirigido a testes</li>
</ul>

<h3>Tipos de testes no jest</h3>
<ul>
    <li><strong>Testes unitarios</strong>: Testa uma parte da aplicação de forma isolada. Ex.: Testa uma função bem especifica
     que faz algo, por exemplo, bem isolada da aplicação</li>
    <li><strong>Testes de integração</strong>: São testes que vão tester o fluxo de uma rota inteira da aplicação.</li>
</ul>