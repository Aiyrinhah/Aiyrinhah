@@ -0,0 +1,14 @@
 # Site acessível sobre Tropicália
 # Sobre
 Refatoração de um site implementando recursos de acessibilidade no html, css e JS.
 ## Recursos de acessibilidade
 - Atributos aria
 - alt
 - tab-index
 - menu de acessibilidade
 ## Tecnologias utilizadas
 - Bootstrap
 - ScrollRevealjs
 - HTML
 - CSS
 - JS

         <section id="tropicalia" class="my-5 pt-6 secao-tropicalia" tabindex="0" aria-label="Seção explicativa sobre a tropicália">
             <div class="container d-flex align-items-center ">
                 <div class="col-4 d-flex justify-content-center fundo-galeria">
                 <div class="col-4 d-flex justify-content-center ">
                     <img src="img/image (1).png" class="rounded-pill" width="273" height="331" loading="lazy">
                 </div>
                 <div class="col-5">
                     <h2>O que foi a Tropicália?</h2>
                     <p class="p-2">A Tropicália, também conhecida como Tropicalismo, foi um movimento cultural
                         brasileiro que surgiu na década de 1960, tendo seu auge entre 1967 e 1968. Esse movimento
                         abrangeu várias expressões artísticas, como a música, o cinema, o teatro e as artes plásticas, e
                         teve como principal característica a mistura de elementos da cultura brasileira tradicional com
                         influências estrangeiras, especialmente do rock e da música pop. Fonte: Site Toda a matéria</p>
                 </div>
             </div>
         </section>
 
         <section id="galeria" tabindex="0" aria-label="Seção de galeria de imagens">
             <h2 class="text-center pt-5">Galeria</h2>
             <div class="container p-3 mt-3 fundo-galeria ">
 
                 <div class="row justify-content-md-center">
                     <div class="col-md-4">
                         <img src="img/lossy-page1-640px-Jorge_Ben_e_o_Trio_Mocotó_no_Teatro_da_Lagoa,_1971.tif.jpg"
                             class="img-fluid rounded-5" loading="lazy">
                     </div>
                     <div class="col-md-4">
                         <img src="img/lossy-page1-640px-Os_Mutantes_2.tif.jpg" class="img-fluid rounded-5"
                             loading="lazy">
                     </div>
                 </div>
                 <div class="row mt-4  justify-content-md-center">
                     <div class="col-md-4">
                         <img src="img/lossy-page1-640px-Gilberto_Gil_nos_anos_1960.tif.jpg" class="img-fluid rounded-5" loading="lazy">
                     </div>
                     <div class="col-md-4">
                         <img src="img/lossy-page1-640px-Caetano_Veloso_no_III_Festival_da_Música_Popular.tif.jpg"
                             class="img-fluid rounded-5" loading="lazy">
                     </div>
                 </div>
              </div>
         </section>
 
         <section id="contato">
             <div class="container p-5 d-flex justify-content-center">
                 <div class="col-md-8 col-lg-10 rounded-5 formulario"> <!-- Caixa do formulário com 60% de largura -->
                     <h2 class="mb-3">Entre em contato</h2>
                     <form>
                         <div class="form-group mb-3">
                             <label for="nome">Nome</label>
                             <input type="text" id="nome" name="nome" class="form-control rounded-3 mt-1"
                                 placeholder="Digite seu nome completo">
                         </div>
                         <div class="form-group mb-3">
                             <label for="email">Email</label>
                             <input type="email" id="email" name="email" class="form-control rounded-3 mt-1"
                                 placeholder="Digite seu email">
                         </div>
                         <div class="form-group mb-3">
                             <label for="mensagem">Mensagem</label>
                             <textarea id="mensagem" name="mensagem" class="form-control rounded-4 mt-2" rows="4"
                                 placeholder="Escreva sua mensagem"></textarea>
                         </div>
                         <div class="d-grid gap-2">
                             <button type="submit" class="btn btn-primary btn-lg rounded-pill">Enviar
                                 mensagem</button>
                         </div>
                     </form>
                 </div>
             </div>
         </section>
     </main>
     <footer class="text-center p-3 fst-italic">
         <p>Acesse nossas redes:</p>
         <i class="bi bi-whatsapp"></i>
         <i class="bi bi-instagram"></i>
         <i class="bi bi-tiktok"></i>
         <p class="mt-3">Desenvolvido por Start by Alura. Projeto fictício sem fins comerciais.</p>
     </footer>
     <script src="https://cdnjs.cloudflare.com/ajax/libs/scrollReveal.js/4.0.9/scrollreveal.js"></script>
     <script src="script.js"></script>
 
 </body>
@@ -0,0 +1,137 @@
 <!DOCTYPE html>
 <html lang="pt-br">
 
 <head>
     <meta charset="UTF-8">
     <meta name="viewport" content="width=device-width, initial-scale=1">
     <link rel="preconnect" href="https://fonts.googleapis.com">
     <title>Tropicália</title>
     <link href="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.3/css/bootstrap.min.css" rel="stylesheet">
     <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/bootstrap-icons/1.11.3/font/bootstrap-icons.min.css">
     <link rel="stylesheet" href="styles.css">
 </head>
 
 <body>
     <header class=" p-5">
 
         <nav class="container d-flex justify-content-between align-items-center" >
             <img src="img/logo.png" class="nav-img " loading="lazy">
             <ul class="nav mt-5">
                 <li class="nav-item"><a class="nav-link" href="#inicio">Início</a></li>
                 <li class="nav-item"><a class="nav-link" href="#galeria">Galeria</a></li>
                 <li class="nav-item"><a class="nav-link" href="#contato">Contato</a></li>
             </ul>
             <div id="acessibilidade" class="menu-acessibilidade"> 
                 <button id="botao-acessibilidade" class="btn btn-primary fw-bold rotacao-botao" aria-expanded="false">acessibilidade</button>
                 <div id="opcoes-acessibilidade" class="opcoes-acessibilidade apresenta-lista">
                     <button id="aumentar-fonte" class="btn btn-primary fw-bold" aria-label="Aumentar o tamanho da fonte">A+</button>
                     <button id="diminuir-fonte" class="btn btn-primary fw-bold" aria-label="diminuir o tamanho da fonte">A-</button>
                     <button id="alterna-contraste" class="btn btn-primary fw-bold"> <i class="bi bi-shadows"></i></button>         
                 </div>
             </div>
         </nav>
        
     </header>
 
 
     <main class="container my-5">
 
         <section id="inicio" class="my-5">
             <div class="inicio-fundo d-flex justify-content-between align-items-center">
                 <div class="esquerda-conteudo">
                     <h1 class="display-4 text-white fst-italic fw-bold">Boas-vindas a</h1>
                     <img src="img/logo-2.png" class="mb-3" width="563"
                         height="278" loading="lazy">
                     <a href="#tropicalia"
                         class="btn btn-primary btn-lg botao-inicio fw-semibold">Quero
                         conhecer!</a>
                 </div>
                 <img src="img/lossy-page1-640px-Os_Mutantes.tif (1).png" alt="A imagem apresenta o grupo musical Os mutantes, sao tres pessoas cantando em um microfone" title="Os mutantes - CC0 Domínio Público / Acervo Arquivo Nacional" class="img-fluid img-inicio">
 
               </div>
         </section>
 
         <section id="tropicalia" class="my-5 pt-6 secao-tropicalia" tabindex="0" aria-label="Seção explicativa sobre a tropicália">
             <div class="container d-flex align-items-center ">
                 <div class="col-4 d-flex justify-content-center fundo-galeria">
                     <img src="img/image (1).png" class="rounded-pill" width="273" height="331" loading="lazy">
                 </div>
                 <div class="col-5">
                     <h2>O que foi a Tropicália?</h2>
                     <p class="p-2">A Tropicália, também conhecida como Tropicalismo, foi um movimento cultural
                         brasileiro que surgiu na década de 1960, tendo seu auge entre 1967 e 1968. Esse movimento
                         abrangeu várias expressões artísticas, como a música, o cinema, o teatro e as artes plásticas, e
                         teve como principal característica a mistura de elementos da cultura brasileira tradicional com
                         influências estrangeiras, especialmente do rock e da música pop. Fonte: Site Toda a matéria</p>
                 </div>
             </div>
         </section>
 
         <section id="galeria" tabindex="0" aria-label="Seção de galeria de imagens">
             <h2 class="text-center pt-5">Galeria</h2>
             <div class="container p-3 mt-3 fundo-galeria ">
 
                 <div class="row justify-content-md-center">
                     <div class="col-md-4">
                         <img src="img/lossy-page1-640px-Jorge_Ben_e_o_Trio_Mocotó_no_Teatro_da_Lagoa,_1971.tif.jpg"
                             class="img-fluid rounded-5" loading="lazy">
                     </div>
                     <div class="col-md-4">
                         <img src="img/lossy-page1-640px-Os_Mutantes_2.tif.jpg" class="img-fluid rounded-5"
                             loading="lazy">
                     </div>
                 </div>
                 <div class="row mt-4  justify-content-md-center">
                     <div class="col-md-4">
                         <img src="img/lossy-page1-640px-Gilberto_Gil_nos_anos_1960.tif.jpg" class="img-fluid rounded-5" loading="lazy">
                     </div>
                     <div class="col-md-4">
                         <img src="img/lossy-page1-640px-Caetano_Veloso_no_III_Festival_da_Música_Popular.tif.jpg"
                             class="img-fluid rounded-5" loading="lazy">
                     </div>
                 </div>
              </div>
         </section>
 
         <section id="contato">
             <div class="container p-5 d-flex justify-content-center">
                 <div class="col-md-8 col-lg-10 rounded-5 formulario"> <!-- Caixa do formulário com 60% de largura -->
                     <h2 class="mb-3">Entre em contato</h2>
                     <form>
                         <div class="form-group mb-3">
                             <label for="nome">Nome</label>
                             <input type="text" id="nome" name="nome" class="form-control rounded-3 mt-1"
                                 placeholder="Digite seu nome completo">
                         </div>
                         <div class="form-group mb-3">
                             <label for="email">Email</label>
                             <input type="email" id="email" name="email" class="form-control rounded-3 mt-1"
                                 placeholder="Digite seu email">
                         </div>
                         <div class="form-group mb-3">
                             <label for="mensagem">Mensagem</label>
                             <textarea id="mensagem" name="mensagem" class="form-control rounded-4 mt-2" rows="4"
                                 placeholder="Escreva sua mensagem"></textarea>
                         </div>
                         <div class="d-grid gap-2">
                             <button type="submit" class="btn btn-primary btn-lg rounded-pill">Enviar
                                 mensagem</button>
                         </div>
                     </form>
                 </div>
             </div>
         </section>
     </main>
     <footer class="text-center p-3 fst-italic">
         <p>Acesse nossas redes:</p>
         <i class="bi bi-whatsapp"></i>
         <i class="bi bi-instagram"></i>
         <i class="bi bi-tiktok"></i>
         <p class="mt-3">Desenvolvido por Start by Alura. Projeto fictício sem fins comerciais.</p>
     </footer>
     <script src="https://cdnjs.cloudflare.com/ajax/libs/scrollReveal.js/4.0.9/scrollreveal.js"></script>
     <script src="script.js"></script>
   
 </body>

 <html lang="pt-br">
 
 <head>
     <meta charset="UTF-8">
     <meta name="viewport" content="width=device-width, initial-scale=1">
     <link rel="preconnect" href="https://fonts.googleapis.com">
     <title>Tropicália</title>
     <link href="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.3/css/bootstrap.min.css" rel="stylesheet">
     <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/bootstrap-icons/1.11.3/font/bootstrap-icons.min.css">
     <link rel="stylesheet" href="styles.css">
 </head>
 
 <body>
     <header class=" p-5">
 
         <nav class="container d-flex justify-content-between align-items-center" >
             <img src="img/logo.png" class="nav-img " loading="lazy">
             <ul class="nav mt-5">
                 <li class="nav-item"><a class="nav-link" href="#inicio">Início</a></li>
                 <li class="nav-item"><a class="nav-link" href="#galeria">Galeria</a></li>
                 <li class="nav-item"><a class="nav-link" href="#contato">Contato</a></li>
             </ul>
             <div id="acessibilidade" class="menu-acessibilidade"> 
                 <button id="botao-acessibilidade" class="btn btn-primary fw-bold rotacao-botao" aria-expanded="false">acessibilidade</button>
                 <div id="opcoes-acessibilidade" class="opcoes-acessibilidade apresenta-lista">
                     <button id="aumentar-fonte" class="btn btn-primary fw-bold" aria-label="Aumentar o tamanho da fonte">A+</button>
                     <button id="diminuir-fonte" class="btn btn-primary fw-bold" aria-label="diminuir o tamanho da fonte">A-</button>
                     <button id="alterna-contraste" class="btn btn-primary fw-bold"> <i class="bi bi-shadows"></i></button>         
                 </div>
             </div>
         </nav>
        
     </header>
 
 
     <main class="container my-5">
 
         <section id="inicio" class="my-5">
             <div class="inicio-fundo d-flex justify-content-between align-items-center">
                 <div class="esquerda-conteudo">
                     <h1 class="display-4 text-white fst-italic fw-bold">Boas-vindas a</h1>
                     <img src="img/logo-2.png" class="mb-3" width="563"
                         height="278" loading="lazy">
                     <a href="#tropicalia"
                         class="btn btn-primary btn-lg botao-inicio fw-semibold">Quero
                         conhecer!</a>
                 </div>
                 <img src="img/lossy-page1-640px-Os_Mutantes.tif (1).png" alt="A imagem apresenta o grupo musical Os mutantes, sao tres pessoas cantando em um microfone" title="Os mutantes - CC0 Domínio Público / Acervo Arquivo Nacional" class="img-fluid img-inicio">
 
               </div>
         </section>
 
         <section id="tropicalia" class="my-5 pt-6 secao-tropicalia" tabindex="0" aria-label="Seção explicativa sobre a tropicália">
             <div class="container d-flex align-items-center ">
                 <div class="col-4 d-flex justify-content-center fundo-galeria">
                     <img src="img/image (1).png" class="rounded-pill" width="273" height="331" loading="lazy">
                 </div>
                 <div class="col-5">
                     <h2>O que foi a Tropicália?</h2>
                     <p class="p-2">A Tropicália, também conhecida como Tropicalismo, foi um movimento cultural
                         brasileiro que surgiu na década de 1960, tendo seu auge entre 1967 e 1968. Esse movimento
                         abrangeu várias expressões artísticas, como a música, o cinema, o teatro e as artes plásticas, e
                         teve como principal característica a mistura de elementos da cultura brasileira tradicional com
                         influências estrangeiras, especialmente do rock e da música pop. Fonte: Site Toda a matéria</p>
                 </div>
             </div>
         </section>
 
         <section id="galeria" tabindex="0" aria-label="Seção de galeria de imagens">
             <h2 class="text-center pt-5">Galeria</h2>
             <div class="container p-3 mt-3 fundo-galeria ">
 
                 <div class="row justify-content-md-center">
                     <div class="col-md-4">
                         <img src="img/lossy-page1-640px-Jorge_Ben_e_o_Trio_Mocotó_no_Teatro_da_Lagoa,_1971.tif.jpg"
                             class="img-fluid rounded-5" loading="lazy">
                     </div>
                     <div class="col-md-4">
                         <img src="img/lossy-page1-640px-Os_Mutantes_2.tif.jpg" class="img-fluid rounded-5"
                             loading="lazy">
                     </div>
                 </div>
                 <div class="row mt-4  justify-content-md-center">
                     <div class="col-md-4">
                         <img src="img/lossy-page1-640px-Gilberto_Gil_nos_anos_1960.tif.jpg" class="img-fluid rounded-5" loading="lazy">
                     </div>
                     <div class="col-md-4">
                         <img src="img/lossy-page1-640px-Caetano_Veloso_no_III_Festival_da_Música_Popular.tif.jpg"
                             class="img-fluid rounded-5" loading="lazy">
                     </div>
                 </div>
              </div>
         </section>
 
         <section id="contato">
             <div class="container p-5 d-flex justify-content-center">
                 <div class="col-md-8 col-lg-10 rounded-5 formulario"> <!-- Caixa do formulário com 60% de largura -->
                     <h2 class="mb-3">Entre em contato</h2>
                     <form>
                         <div class="form-group mb-3">
                             <label for="nome">Nome</label>
                             <input type="text" id="nome" name="nome" class="form-control rounded-3 mt-1"
                                 placeholder="Digite seu nome completo">
                         </div>
                         <div class="form-group mb-3">
                             <label for="email">Email</label>
                             <input type="email" id="email" name="email" class="form-control rounded-3 mt-1"
                                 placeholder="Digite seu email">
                         </div>
                         <div class="form-group mb-3">
                             <label for="mensagem">Mensagem</label>
                             <textarea id="mensagem" name="mensagem" class="form-control rounded-4 mt-2" rows="4"
                                 placeholder="Escreva sua mensagem"></textarea>
                         </div>
                         <div class="d-grid gap-2">
                             <button type="submit" class="btn btn-primary btn-lg rounded-pill">Enviar
                                 mensagem</button>
                         </div>
                     </form>
                 </div>
             </div>
         </section>
     </main>
     <footer class="text-center p-3 fst-italic">
         <p>Acesse nossas redes:</p>
         <i class="bi bi-whatsapp"></i>
         <i class="bi bi-instagram"></i>
         <i class="bi bi-tiktok"></i>
         <p class="mt-3">Desenvolvido por Start by Alura. Projeto fictício sem fins comerciais.</p>
     </footer>
     <script src="https://cdnjs.cloudflare.com/ajax/libs/scrollReveal.js/4.0.9/scrollreveal.js"></script>
     <script src="script.js"></script>
   
 </body>
 
 </html>
 @@ -0,0 +1,43 @@
 document.addEventListener('DOMContentLoaded', function(){
     const botaoDeAcessibilidade = document.getElementById('botao-acessibilidade')
     const opcoesDeAcessibilidade = document.getElementById('opcoes-acessibilidade')
  
     botaoDeAcessibilidade.addEventListener('click', function (){
      botaoDeAcessibilidade.classList.toggle('rotacao-botao');
      opcoesDeAcessibilidade.classList.toggle('apresenta-lista')
  
      const botaoSelecionado = botaoDeAcessibilidade.getAttribute('aria-expanded') === 'true';
      botaoDeAcessibilidade.setAttribute('aria-expanded', !botaoSelecionado)
    
     })
  
      const aumentaFonteBotao = document.getElementById('aumentar-fonte');
      const diminuiFonteBotao = document.getElementById('diminuir-fonte');
      
      const alternaContraste = document.getElementById('alterna-contraste')
  
      let tamanhoAtualFonte = 1;
  
      aumentaFonteBotao.addEventListener('click', function(){
          tamanhoAtualFonte += 0.1;
          document.body.style.fontSize = `${tamanhoAtualFonte}rem`
  
      })
  
      diminuiFonteBotao.addEventListener('click', function(){
          tamanhoAtualFonte -= 0.1;
          document.body.style.fontSize = `${tamanhoAtualFonte}rem`
  
      })
  
      alternaContraste.addEventListener('click', function(){
          document.body.classList.toggle('alto-contraste')
      })
  
  
  })
  
  ScrollReveal().reveal('#inicio', { delay: 500 });
  ScrollReveal().reveal('#tropicalia', { delay: 500 });
  ScrollReveal().reveal('#galeria', { delay: 500 });
  ScrollReveal().reveal('#contato', { delay: 500 });
  @@ -0,0 +1,200 @@
 @import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100..900;1,100..900&display=swap');
 @import url('https://fonts.googleapis.com/css2?family=Lemon&display=swap');
 
 :root {
     --laranja-claro: #FF862A;
     --alto-contraste-fundo: #000000;
     --alto-contraste-texto: #ffffff;
     --alto-contraste-link: #ffd700;
 }
 
 body {
     font-size: 1rem;
     font-family: 'Montserrat';
 }
 
 header {
     background-color: #ffffff;
 }
 
 
 section {
     padding-bottom: 5rem;
 }
 
 
 .nav-link {
     color: #CB6D43;
     font-weight: 600;
 }
 
 .inicio-fundo {
     /* aula 3 */
     background-image: url('img/4965007.jpg');
     /* Substitua pelo caminho da sua imagem */
     background-size: cover;
     background-position: right;
     border-radius: 80px;
     width: 100%;
     height: 606px;
     padding: 40px;
     margin: 0 auto;
 }
 
 /* posicionamento para a imagem à direita */
 .img-inicio {
     position: absolute;
     right: 0;
     top: 18rem;
     width: 45rem;
     height: auto;
 }
 
 
 .esquerda-conteudo {
     display: flex;
     flex-direction: column;
     align-items: flex-start;
     gap: 1rem;
 }
 
 
 .botao-inicio {
     background-color: var(--laranja-claro);
     border-radius: 30px;
     border: none;
     width: 14em;
     height: 3em;
     align-content: center;
 
 }
 
 .display-4 {
     text-shadow: -5px 5px var(--laranja-claro);
 }
 
 
 #tropicalia {
     position: relative;
     padding-top: 5rem;
     margin-top: 3rem;
     margin-bottom: 3rem;
     background: url('img/flor.png') top right no-repeat,
         url('img/flor-esquerda.png') bottom left no-repeat;
     background-size: 180px 180px;
     /* Ajuste o tamanho conforme necessário */
 }
 
 #tropicalia .container {
     display: flex;
     align-items: center;
     justify-content: center;
     position: relative;
     z-index: 1;
     /* Garante que o conteúdo fica acima das imagens do background */
 }
 
 
 h2 {
     font-family: 'Lemon', serif;
     font-size: 2.5em;
     font-style: normal;
     color: var(--laranja-claro);
 }
 
 #galeria {
     background-color: #FAF4F4;
 
 }
 
 .fundo-galeria {
     background: url('img/flor-bottom-direita.png') bottom right no-repeat;
     background-size: 180px 180px;
 }
 
 #contato {
     background-image: url('img/4965007.jpg');
     background-size: cover;
     padding: 4rem 0;
     /* Espaçamento interno para a seção de contato */
 
 }
 
 .formulario {
     background-color: #ffffff;
     padding: 2rem;
     /* Espaçamento interno dentro do formulário */
     border-radius: 10px;
     /* Borda arredondada para o formulário */
     box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
     /* Sombra suave para destacar o formulário */
     font-weight: bold;
 }
 
 .formulario button {
     background-color: #CB6D43;
     border: none;
     font-weight: bold;
 }
 
 .form-control {
     background-color: #F1EDEF;
 }
 .menu-acessibilidade{
     position: fixed;
     top:2rem;
     right:20px;
     z-index: 1000;
 }
 
 .rotacao-botao{
     transform: rotate(-90deg);
     transform-origin: right center;
 }
 
 .opcoes-acessibilidade{
     margin-top:10px;
     display: flex;
     flex-direction: column;
 }
 
 .opcoes-acessibilidade button{
     margin-bottom: 5px;
 }
 .apresenta-lista{
     display: none;
 }
 
 .alto-contraste{
     background-color: var(--alto-contraste-fundo);
     color: var(--alto-contraste-texto);
 }
 
 .alto-contraste header,
 .alto-contraste footer,
 .alto-contraste .formulario{
     background-color: var(--alto-contraste-fundo);
     color: var(--alto-contraste-texto);
 }
 
 .alto-contraste .nav-link{
     color: var(--alto-contraste-link);
 }
 
 .alto-contraste .botao-inicio,
 .alto-contraste .formulario button,
 .alto-contraste .btn-primary{
     background-color: var(--alto-contraste-link);
     color: var(--alto-contraste-fundo)
 }
 
 .alto-contraste #tropicalia {
     background: none;
 }
 
 .alto-contraste #galeria {
     background-color: var(--alto-contraste-fundo);
 }
 .alto-contraste .fundo-galeria {
     background: none;
 }
 
 
