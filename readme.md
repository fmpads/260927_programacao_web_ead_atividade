# 27/9/26

Faculdade Municipal da Palhoça
Análise e Desenvolvimento de Sistemas
Programação Web
Docente: Leandro Pickler
Discente: Jean Douglas Toledo Rodrigues Junior

# EAD

# 1 Quando usar a tag div

A tag <div> cria uma divisão ou um agrupamento dentro do corpo da página.
Ela não possui um significado visual por conta própria. Sua função é reunir elementos relacionados para que possam ser organizados, posicionados ou formatados em conjunto com CSS.
Exemplo de uso: uma página pode ter uma <div> para o cartão de apresentação de um aluno. Dentro desse grupo podem existir um título, um parágrafo, uma imagem, uma lista e um link.

HTML

<div class="cartao">
 <h2>Maria Silva</h2>
 <p>Estudante de Análise e Desenvolvimento de Sistemas.</p>
 <a href="https://www.fmpsc.edu.br">Conheça a FMP</a>
</div>

O atributo class recebeu o nome cartao. Esse nome permite selecionar a <div> no CSS e aplicar a mesma formatação a todos os elementos que utilizarem essa classe.

# O que pode ficar dentro de uma div

Conteúdo Exemplos Finalidade
Títulos e textos <h1>, <h2>, <p>, <span> Apresentar informações e destacar partes do texto.Imagens e links <img>, <a> Exibir imagens e permitir navegação.
Listas <ul>, <ol>, <li> Organizar itens com ou sem numeração.
Formulários <form>, <label>, <input> Agrupar campos que recebem dados do usuário.Outras divisões <div> Criar grupos internos quando a organização exigir.

# Boas práticas

 Use nomes de classe que expliquem a função do grupo, como cartao, conteudo ou aviso.  Evite criar várias <div> sem necessidade. Quando houver significado próprio, prefira tags como <header>, <main>, <section>, <article> e <footer>.
 Não coloque <head>, <html> ou <body> dentro de uma <div>. A <div> deve ficar dentro do <body>.

# 2 O que colocar dentro do head

O <head> reúne informações e configurações sobre a página. Em geral, esses dados não aparecem como conteúdo na área principal do navegador, mas ajudam o navegador, os mecanismos de busca e os
dispositivos a interpretar o documento corretamente.

Elemento Função

<meta charset="UTF-8">      Define a codificação e permite exibir corretamente acentos e caracteres especiais.
<meta name="viewport">      Ajusta a largura da página para celulares, tablets e outros dispositivos.
<title>                     Define o texto exibido na aba do navegador.
<style>                     Permite escrever as regras CSS dentro do próprio arquivo index.html.

# Exemplo de head

HTML

<head>
 <meta charset="UTF-8">
 <meta name="viewport" content="width=device-width, initial-scale=1.0">
 <title>Minha apresentação</title>
 <style>
 h1 { color: #17365D; }
 p { color: #333333; }
 </style>
</head>

O título mostrado dentro da página deve ficar no <body>, normalmente com <h1>. Já o <title> do <head> aparece na aba do navegador. São funções diferentes.

HTML

<body>
 <h1>Minha apresentação</h1>
 <p>Este conteúdo aparece na página.</p>
</body>

# Como colorir um texto usando CSS

A propriedade color altera a cor do texto. No CSS, uma regra é formada pelo seletor, pela propriedade e
pelo valor. No exemplo abaixo, o seletor h1 localiza todos os títulos <h1>, color é a propriedade e #17365D é o valor da cor.

CSS
h1 {
color: #17365D;
}

Exemplo visual: este texto está em azul escuro porque recebeu a propriedade color.

Formas de informar uma cor
Formato Exemplo Observação
Nome color: blue; Simples, mas oferece uma quantidade limitada de nomes.
Hexadecimal color: #17365D; Muito utilizado em projetos e identidades visuais.
RGB color: rgb(23, 54, 93); Define as intensidades de vermelho, verde e azul.Como aplicar o CSS dentro do index html

# Nesta atividade, as regras CSS devem ficar dentro da tag <style>, localizada no <head> do arquivo index.html.

HTML

<style>
 h1 {
 color: #17365D;
 }
 p {
 color: green;
 }
</style>

Também é possível aplicar uma regra diretamente no elemento. Essa forma é chamada CSS inline e deve ser usada apenas em exemplos simples ou situações pontuais.

HTML

<p style="color: red;">Texto em vermelho</p>

# Exemplo completo de página

Crie uma pasta chamada atividade-html e salve nela o arquivo index.html. A estrutura, o conteúdo e as regras CSS ficarão reunidos nesse único arquivo.

Arquivo index.html

<!DOCTYPE html>
<html lang="pt-BR">
<head>
 <meta charset="UTF-8">
 <meta name="viewport" content="width=device-width, initial-scale=1.0">
 <title>Minha apresentação</title>
 <style>
 body {
 margin: 0;
 font-family: Arial, sans-serif;
 background-color: #f2f5f8;
 color: #333333;
 }
 main {
 width: 80%;
 max-width: 700px;
 margin: 40px auto;
 }
 h1 {
 color: #17365D;
 text-align: center;
 }
 .cartao {
 background-color: white;
 padding: 24px;
 border: 1px solid #d9d9d9;
 }
 .destaque {
 color: #2E7D32;
 font-weight: bold;
 }
 </style>
</head>
<body>
 <main>
 <h1>Minha apresentação</h1>
 <div class="cartao">
 <h2>João da Silva</h2>
 <p class="destaque">Estudante de ADS</p>
 <p>Estou aprendendo HTML e CSS para criar páginas web.</p>
 <h3>Assuntos que estou estudando</h3>
 <ul>
 <li>Estrutura de uma página HTML</li>
 <li>Uso de div para agrupar conteúdos</li>
 <li>Cores e estilos com CSS</li>
 </ul>
 </div>
 </main>
</body>
</html>

# Como interpretar o resultado

 O <head> configura a página e contém as regras CSS dentro da tag <style>.
 O <main> identifica o conteúdo principal.
 A <div class="cartao"> agrupa os dados de apresentação.
 O seletor .cartao aplica estilo ao elemento que possui a classe cartao.
 Os seletores h1, .cartao h2 e .destaque aplicam cores a textos diferentes.

# Teste no navegador

1. Salve o arquivo com o nome index.html.
2. Abra o arquivo index.html em um navegador.
3. Altere uma cor dentro da tag <style>, salve o arquivo e atualize a página.
4. Experimente criar uma segunda <div> com outro conteúdo.

# Atividade prática

Crie uma página chamada Meu perfil acadêmico. A página deverá apresentar informações sobre você, sua formação e um tema de tecnologia que deseja aprender. Utilize os exemplos anteriores como referência, mas escreva seus próprios conteúdos. Além de entregar o código completo, você deverá explicar como organizou a página e como utilizou o HTML e o CSS.

# Requisitos da página

1. Criar o arquivo index.html com a estrutura completa: <!DOCTYPE html>, <html>, <head> e <body>.
2. No <head>, incluir charset UTF-8, viewport, title e a tag <style>.
3. No <body>, criar um <h1> com o título Meu perfil acadêmico.
4. Criar pelo menos duas <div> com classes diferentes, por exemplo perfil e objetivos.
5. Na primeira <div>, inserir um título, dois parágrafos e uma lista com três interesses.
6. Na segunda <div>, inserir um título e um texto sobre o que deseja aprender em tecnologia.
7. Dentro da tag <style>, aplicar pelo menos três cores de texto usando a propriedade color.
8. Aplicar também background-color, padding e border em pelo menos uma <div>.
9. Testar a página no navegador e corrigir eventuais erros antes da entrega.
   Explicação obrigatória do código
   Depois de concluir a página, prepare uma explicação com suas próprias palavras. Copie cada pergunta abaixo e escreva de duas a quatro frases para respondê-la. Sempre que possível, cite uma parte do seu código.

## EXPLICAÇÃO DA ATIVIDADE

## 10. Como você montou a estrutura básica do arquivo index.html? Explique a função de <!DOCTYPE html>, <html>, <head> e <body>.

Eu organizei a página com a estrutura padrão do HTML. O documento começa com <!DOCTYPE html>, que informa ao navegador que o arquivo é HTML5. Em seguida, usei a tag <html lang="pt-BR"> para abrir o documento em português do Brasil. Dentro do <head> coloquei informações da página, como o charset, a viewport e o título. Já o <body> foi usado para armazenar todo o conteúdo visível da página, como o título principal e as divs com os textos.

## 11. O que você colocou dentro do <head> e qual é a função de cada elemento utilizado?

Dentro do <head> incluí <meta charset="UTF-8"> para permitir acentos e letras especiais; <meta name="viewport" content="width=device-width, initial-scale=1.0"> para ajustar a página em celulares e tablets; <title>Meu perfil acadêmico</title> para definir o nome da aba do navegador; e a tag <style> para escrever o CSS da página. Essa parte do código foi importante porque organiza e define a aparência da página antes do conteúdo aparecer na tela.

## 12. Como você utilizou as duas <div> para separar e organizar os conteúdos da página? Informe também os nomes das classes criadas.

Usei duas divs para separar os conteúdos em blocos com funções diferentes. A primeira div tem a classe perfil e foi usada para apresentar informações pessoais e os interesses acadêmicos. A segunda div tem a classe objetivos e foi usada para explicar o que desejo aprender em tecnologia. Essa organização deixou a página mais clara e facilitou aplicar estilos diferentes para cada parte.

## 13. Como você aplicou o CSS dentro da tag <style>? Apresente um seletor, uma propriedade e um valor existentes no seu código.

O CSS foi colocado dentro da tag <style> no <head>. Um exemplo é o seletor h1, a propriedade color e o valor #17365D, que define a cor azul escura do título principal. Também usei background-color, padding e border para decorar as divs e deixá-las com melhor visual. Isso foi feito para melhorar a leitura e a organização da página.

## 14. Quais cores e propriedades visuais você escolheu e qual foi o resultado observado no navegador?

Escolhi uma paleta com tons de azul, verde, vermelho e cinza para dar uma aparência limpa e profissional. O título principal ficou em azul escuro, os títulos das divs ficaram em verde e a frase destacada ficou em vermelho. Além disso, apliquei background-color para o fundo das caixas, padding para dar espaço interno e border para separar os blocos. O resultado foi uma página simples, organizada e fácil de ler.

## 15. Qual alteração ou correção foi necessária depois que você testou a página? Caso não tenha ocorrido erro, explique como realizou o teste.

No meu processo de teste, revisei o código para verificar se as tags estavam fechadas corretamente e se os estilos estavam aplicando às divs e aos textos. Como a estrutura foi montada de forma simples, não foi necessário corrigir erros grandes. O teste foi feito abrindo o arquivo index.html em um navegador e conferindo se o layout e as cores apareceram como planejado.

## 16. Organização do material

O material ficou organizado em dois arquivos: o arquivo index.html com todo o HTML e o CSS dentro do <style>, e este documento com a explicação da atividade. O objetivo foi manter o trabalho simples e completo.

## 17. Postar o link do GitHub.
