# guaratur-materialize

Passo 1: Criação da Página "Acomodações em Guarapuava"

Crie uma nova página em seu site chamada "Acomodações em Guarapuava." Certifique-se de que a página esteja acessível no menu de navegação superior (navbar) e na barra lateral (sidenav) do site.
Passo 2: Baixar Dependências com NPM e Configurar o package.json

Antes de prosseguir, certifique-se de que você possui todas as dependências necessárias para o desenvolvimento do projeto, incluindo o framework Materialize CSS. Como o arquivo package.json não está presente, você precisará configurá-lo e adicionar as dependências manualmente.

Se você não tem um arquivo package.json, você pode criá-lo manualmente na pasta raiz do projeto. Para criar o arquivo package.json, abra um terminal na pasta do projeto e execute o seguinte comando:

npm init -y
Isso criará um arquivo package.json com valores padrão.

Em seguida, você pode adicionar o framework Materialize CSS como uma dependência ao arquivo package.json utilizando o seguinte comando:

npm install materialize-css@next
Isso instalará a versão mais recente do Materialize CSS em seu projeto.

Agora, você deve atualizar as referências no HTML para que apontem para a pasta node_modules. No seu arquivo HTML, onde você inclui o Materialize CSS, certifique-se de que a referência esteja como:

<link rel="stylesheet" href="node_modules/materialize-css/dist/css/materialize.min.css">
Passo 3: Avaliação Inicial dos Paineis

Acesse o site Guaratur e navegue até as páginas que contêm os painéis "Entre em Contato," "Formulário de Contato" e "Localização."
Faça uma avaliação inicial da aparência e do layout dos painéis nos dispositivos móveis (smartphones e tablets), notebooks e computadores de mesa, utilizando as ferramentas de desenvolvedor do navegador Google Chrome. Observe quaisquer problemas de layout ou necessidades de reorganização.
No Google Chrome, clique com o botão direito do mouse em qualquer parte da página e selecione "Inspecionar" ou pressione as teclas "Ctrl+Shift+I" (Windows/Linux) ou "Cmd+Option+I" (Mac) para abrir as ferramentas de desenvolvedor. Você também pode pressionar a tecla F12 para abrir as ferramentas de desenvolvedor diretamente.
No painel de ferramentas de desenvolvedor, você verá um ícone de dispositivo no canto superior esquerdo (ícone de telefone e tablet). Clique nele para ativar a visualização responsiva.
Passo 4: Edição dos Paineis e Cores do Materialize CSS

Utilizando as classes e recursos do framework Materialize CSS, edite os painéis existentes e aplique as cores do Materialize CSS que achar necessárias. Assegure os seguintes requisitos de responsividade:

Em telas de celular e tablet:

Os painéis "Entre em Contato" e "Formulário de Contato" devem ser organizados um abaixo do outro, ocupando a largura total da tela, sem offset.
O painel "Localização" deve ser escondido.
Em notebooks e computadores de mesa:

Os painéis "Entre em Contato" e "Formulário de Contato" devem ser organizados um abaixo do outro, ocupando a largura total da tela, com um offset de 3 colunas.
O painel "Localização" deve ocupar a largura total da tela.
Passo 5: Uso de Cards para Representar Acomodações

Na nova página "Acomodações em Guarapuava," apresente uma lista de diferentes acomodações disponíveis na cidade, incluindo pelo menos 6 opções que podem ser hotéis e pousadas. Use cards para representar cada acomodação. Cada card deve conter:

Uma foto representativa da acomodação: Para fazer isso, crie uma conta no Cloudinary (https://cloudinary.com/) e utilize sua interface gráfica para fazer o upload das imagens das acomodações. Após o upload, o Cloudinary gera URLs para as imagens, que você pode referenciar no código HTML da página.
O nome do hotel ou pousada.
Uma breve descrição da acomodação.
Os preços médios por noite.
Uma classificação de estrelas (de 1 a 5) ou uma nota de avaliação (de 0 a 10) para cada acomodação.
Passo 6: Teste de Responsividade e Cores

Teste a página de "Acomodações em Guarapuava" e os painéis editados em diferentes dispositivos (celulares, tablets, notebooks e computadores de mesa) para garantir que eles tenham uma aparência e funcionalidade adequadas em cada tamanho de tela, com as cores do Materialize CSS aplicadas.
Para testar a responsividade, utilize a ferramenta "Mobile simulator - responsive testing tool" (https://chrome.google.com/webstore/detail/mobile-simulator-responsi/ckejmhbmlajgoklhgbapkiccekfoccmk) ou a extensão "Responsive Viewer" (https://chrome.google.com/webstore/detail/responsive-viewer/inmopeiepgfljkpkidclfgbgbmfcennb) no navegador Google Chrome.
Passo opcional: Ajuste a Responsividade do Texto nos Títulos dos Cards

Neste passo, você deve garantir que o tamanho do texto nos títulos dos cards de informações gerais (seletor h4) e de pontos turísticos (seletor .card-image .card-title) seja responsivo, ajustando-o para diferentes tamanhos de tela. Você deve usar a função CSS clamp, min ou max para especificar um tamanho de fonte responsivo.

Aqui está um exemplo de como você deve aplicar a função clamp nos títulos dos cards:

/* Título dos cards de informações gerais */
h4 { font-size: clamp(1.3rem, 2vw, 2.6rem); /* Ajuste os valores conforme necessário */ } /* Título dos cards de pontos turísticos */ .card-image .card-title { font-size: clamp(1.2rem, 2.5vw, 3rem); /* Ajuste os valores conforme necessário */ }