🧮 Calculadora Interativa com Vue 3 e Vite

Visão Geral

Este projeto é uma calculadora web simples e funcional, desenvolvida com Vue 3 e Vite. Ele demonstra a implementação de uma interface de usuário reativa para operações aritméticas básicas, utilizando os conceitos fundamentais do Vue, como reactive para gerenciamento de estado e computed para lógica de cálculo em tempo real.

Funcionalidades

•
Operações Básicas: Realiza adição, subtração, multiplicação e divisão.

•
Reatividade: Atualiza o resultado instantaneamente conforme os números e operadores são inseridos.

•
Tratamento de Erros: Inclui tratamento para divisão por zero.

•
Interface Intuitiva: Design limpo e fácil de usar.

Tecnologias Utilizadas

•
Vue 3: Framework progressivo para construção de interfaces de usuário.

•
Vite: Ferramenta de build de próxima geração para desenvolvimento Front-end, oferecendo um ambiente de desenvolvimento rápido e otimizado.

•
JavaScript (ES6+): Lógica de programação.

•
HTML5 & CSS3: Estrutura e estilização da interface.

Estrutura do Projeto

O projeto é composto por um componente principal (App.vue) que gerencia a lógica da calculadora e a renderização da interface, e componentes auxiliares para o formulário de entrada (Formulario.vue) e exibição do resultado (Resultado.vue).

Plain Text


src/
├── components/
│   ├── Formulario.vue      # Componente para entrada de números e seleção de operação
│   └── Resultado.vue       # Componente para exibir o resultado do cálculo
└── App.vue                 # Componente principal da calculadora



Como Instalar e Rodar Localmente

Para ter uma cópia local do projeto em execução, siga estes passos:

Pré-requisitos

Certifique-se de ter o Node.js (versão 20.19.0 ou superior) e o npm (gerenciador de pacotes do Node.js) instalados em sua máquina.

Instalação

1.
Clone o repositório:

Bash


git clone https://github.com/therealherick/Calculadora-vueJS.git





2.
Navegue até o diretório do projeto:

Bash


cd Calculadora-vueJS





3.
Instale as dependências:

Bash


npm install





Rodando a Aplicação

1.
Modo de Desenvolvimento (com Hot-Reload ):

Bash


npm run dev



A aplicação estará disponível em http://localhost:5173 (ou outra porta disponível ).



2.
Modo de Produção (Build):

Bash


npm run build



Isso irá compilar e minificar os arquivos para produção na pasta dist/.



Contribuição

Contribuições são sempre bem-vindas! Se você tiver sugestões de melhoria, novas funcionalidades ou encontrar algum bug, sinta-se à vontade para abrir uma issue ou enviar um pull request.

Licença

Este projeto está licenciado sob a licença MIT. Veja o arquivo LICENSE para mais detalhes. (A ser adicionado posteriormente)

Autor

Herick Gomes

