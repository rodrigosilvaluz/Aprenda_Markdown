# Aprendendo MarkDown!

## Introdução

O Markdown é uma ferramenta de conversão de texto em HTML para escritores da web. 
O Markdown permite que você escreva usando um formato de texto simples, fácil de ler e de escrever, e depois convertê-lo em XHTML (ou HTML) estruturalmente válido.

Assim, “Markdown” é duas coisas: (1) uma sintaxe de formatação de texto sem formatação; e (2) uma ferramenta de software, escrita em Perl, que converte a formatação de texto sem formatação em HTML. 
Consulte a página [Sintaxe](https://translate.googleusercontent.com/translate_c?depth=1&rurl=translate.google.com&sl=auto&sp=nmt4&tl=pt-BR&u=https://daringfireball.net/projects/markdown/syntax&xid=17259,15700023,15700186,15700191,15700256,15700259,15700262,15700265,15700271,15700280,15700283&usg=ALkJrhg3kUvvAPNty6x2346A6cqVfnSJVA) para obter detalhes relacionados à sintaxe de formatação do Markdown. 

Você pode experimentá-lo agora mesmo, usando o [Dingus](https://translate.googleusercontent.com/translate_c?depth=1&rurl=translate.google.com&sl=auto&sp=nmt4&tl=pt-BR&u=https://daringfireball.net/projects/markdown/dingus&xid=17259,15700023,15700186,15700191,15700256,15700259,15700262,15700265,15700271,15700280,15700283&usg=ALkJrhhsx0WumTxqfymIeyU_nBjgo-7sig) online.

O objetivo principal do design da sintaxe de formatação do Markdown é torná-lo o mais legível possível. A idéia é que um documento no formato Markdown seja publicável como está, como texto sem formatação, sem parecer que foi marcado com tags ou instruções de formatação. Embora a sintaxe do Markdown tenha sido influenciada por vários filtros de texto para HTML existentes, a maior fonte de inspiração para a sintaxe do Markdown é o formato de email em texto sem formatação.

A melhor maneira de ter uma ideia da sintaxe de formatação do Markdown é simplesmente olhar para um documento formatado no Markdown. 
Por exemplo, você pode visualizar a fonte Markdown do texto do artigo nesta página aqui: http://daringfireball.net/projects/markdown/index.text

(Você pode usar este truque de sufixo '.text' para visualizar a fonte Markdown para o conteúdo de cada uma das páginas nesta seção, por exemplo, as páginas Sintaxe e Licença .)

O Markdown é um software livre, disponível sob uma licença de código aberto no estilo BSD. Veja a página Licença para mais informações.
Lista de discussão

Criei uma lista de discussão pública para discussão sobre o Markdown . Qualquer tópico relacionado ao Markdown - tanto sua sintaxe de formatação quanto seu software - é um jogo justo para discussão. Qualquer pessoa interessada é bem-vinda.

Espero que a lista de discussão leve a boas idéias para futuras melhorias no Markdown.
Instalação e Requisitos

O Markdown requer o Perl 5.6.0 ou posterior. Bem-vindo ao século XXI. O Markdown também requer o módulo de biblioteca padrão Perl Digest :: MD5 , que provavelmente já está instalado no seu servidor.
Tipo móvel

O Markdown funciona com o Movable Type versão 2.6 ou posterior (incluindo o Movable Type 3.0).

    Copie o arquivo "Markdown.pl" para o diretório "plugins" do Movable Type. O diretório "plugins" deve estar no mesmo diretório que "mt.cgi"; se o diretório "plugins" ainda não existir, use seu programa FTP para criá-lo. Sua instalação deve ficar assim:

     (mt home)/plugins/Markdown.pl 

    Uma vez instalado, o Markdown aparecerá como uma opção no menu pop-up Formatação de texto do Movable Type. Isso é selecionável por postagem:

   ![Captura de tela do menu Movable Type 'Text Formatting'](https://daringfireball.net/graphics/markdown/mt_textformat_menu.png)

    O Markdown converte suas postagens em HTML quando você publica; as próprias postagens são armazenadas no banco de dados do MT no formato Markdown.

    Se você também instalar o SmartyPants 1.5 (ou posterior), o Markdown oferecerá uma segunda opção de formatação de texto: “Markdown With SmartyPants”. Essa opção é a mesma do formatador "Markdown" comum, exceto que ele usa automaticamente o SmartyPants para criar aspas encaracoladas, traços e elipses tipograficamente corretos. Consulte a página da Web SmartyPants para obter mais informações.

    Para tornar o Markdown (ou "Markdown With SmartyPants") sua opção de formatação de texto padrão para novas postagens, vá para Weblog Config: Preferences. 

Observe que, por padrão, o Markdown produz saída XHTML. Para configurar o Markdown para produzir saída HTML 4, consulte "Configuração", abaixo.
Blosxom

O Markdown funciona com o Blosxom versão 2.0 ou posterior.

    Renomeie o plug-in "Markdown.pl" para "Markdown" (o caso é importante). O tipo móvel requer que os plug-ins tenham uma extensão ".pl"; Blosxom proíbe.

    Copie o arquivo de plug-in “Markdown” para sua pasta de plug-ins Blosxom. Se você não tiver certeza de onde está sua pasta de plug-ins do Blosxom, consulte a documentação do Blosxom para obter informações.

    É isso aí. As entradas no seu blog agora serão processadas automaticamente pelo Markdown.

    Se você deseja aplicar a formatação do Markdown apenas a determinadas postagens, em vez de todas, o Markdown pode opcionalmente ser usado em conjunto com o plug-in Meta da Blosxom. Primeiro, instale o plug-in Meta. Em seguida, abra o arquivo de plug-in Markdown em um editor de texto e defina a variável de configuração $g_blosxom_use_meta como 1. Em seguida, inclua simplesmente uma linha de cabeçalho “ meta-markup: Markdown ” na parte superior de cada postagem que você compõe usando o Markdown. 

BBEdit

O Markdown funciona com o BBEdit 6.1 ou posterior no Mac OS X. Também funciona com o BBEdit 5.1 ou posterior e o MacPerl 5.6.1 no Mac OS 8.6 ou posterior. Se você estiver executando o Mac OS X 10.2 (Jaguar), pode ser necessário instalar o módulo Perl Digest :: MD5 do CPAN; Digest :: MD5 vem pré-instalado no Mac OS X 10.3 (Panther).

    Copie o arquivo “Markdown.pl” para a pasta de filtros apropriada na pasta “BBEdit Support”. No Mac OS X, deve ser:

     BBEdit Support/Unix Support/Unix Filters/ 

    Consulte a documentação do BBEdit para obter mais detalhes sobre o local dessas pastas.

    Você pode renomear "Markdown.pl" para o que quiser.

    É isso aí. Para usar o Markdown, selecione algum texto em um documento do BBEdit e escolha Markdown no submenu Filtros no menu “#!” Ou na paleta flutuante Filtros. 

Configuração

Por padrão, o Markdown produz saída XHTML para tags com elementos vazios. Por exemplo:

 <br /> 

O markdown pode ser configurado para produzir tags no estilo HTML; por exemplo:

 <br> 

Tipo móvel

Você precisa usar uma tag de contêiner MTMarkdownOptions especial em cada modelo de tipo móvel onde deseja saída em estilo HTML 4:

 <MTMarkdownOptions output='html4'> ... put your entry content here ... </MTMarkdownOptions> 

A maneira mais fácil de usar o MTMarkdownOptions é provavelmente colocar a tag de abertura logo após a tag <body> e a tag de fechamento antes de </body> .

Para suprimir o processamento do Markdown em um modelo específico, ou seja, para publicar o texto bruto formatado pelo Markdown sem tradução para (X) HTML, defina o atributo de output como 'raw':

 <MTMarkdownOptions output='raw'> ... put your entry content here ... </MTMarkdownOptions> 

Linha de comando

Use a --html4tags de linha de comando --html4tags para produzir saída HTML a partir de uma linha de comando no estilo Unix. Por exemplo:

 % perl Markdown.pl --html4tags foo.text 

Digite perldoc Markdown.pl ou leia a documentação do POD no código-fonte Markdown.pl para obter mais informações.
Reconhecimentos

Aaron Swartz merece uma enorme quantidade de crédito por seus comentários sobre o design da sintaxe de formatação de Markdown. O Markdown é muito melhor, graças às idéias, feedback e testes de Aaron. Além disso, o html2text do Aaron é um utilitário muito útil (e gratuito) para transformar HTML em texto sem formatação no formato Markdown.

Nathaniel Irons , Dan Benjamin , Daniel Bogan e Jason Perkins também merecem agradecimentos por seus comentários.

Michel Fortin portou o Markdown para o PHP; é uma porta esplêndida e altamente recomendada para quem procura uma implementação PHP do Markdown. 


Obtendo a Sintaxe de Formatação do Gist of Markdown

Esta página oferece uma breve visão geral de como é usar o Markdown. A página de sintaxe fornece documentação completa e detalhada para todos os recursos, mas o Markdown deve ser muito fácil de entender simplesmente observando alguns exemplos em ação. Os exemplos nesta página são escritos no estilo antes / depois, mostrando a sintaxe do exemplo e a saída HTML produzida pelo Markdown.

Também é útil simplesmente experimentar o Markdown; o Dingus é um aplicativo da web que permite digitar seu próprio texto no formato Markdown e traduzi-lo para XHTML.

Nota: Este documento é ele próprio escrito usando Markdown; você pode ver a fonte adicionando '.text' ao URL .
Parágrafos, cabeçalhos, citações em bloco

Um parágrafo é simplesmente uma ou mais linhas consecutivas de texto, separadas por uma ou mais linhas em branco. (Uma linha em branco é qualquer linha que se parece com uma linha em branco - uma linha que não contém nada além de espaços ou tabulações é considerada em branco.) Parágrafos normais não devem ser recuados com espaços ou tabulações.

O Markdown oferece dois estilos de cabeçalhos: Setext e atx . Os cabeçalhos no estilo Setext para <h1> e <h2> são criados por "sublinhado" com sinais de igual ( = ) e hífens ( - ), respectivamente. Para criar um cabeçalho no estilo atx, coloque de 1 a 6 marcas de hash ( # ) no início da linha - o número de hashes é igual ao nível do cabeçalho HTML resultante.

As cotações em bloco são indicadas usando colchetes angulares ' > ' no estilo email.

Remarcação:

 A First Level Header ==================== A Second Level Header --------------------- Now is the time for all good men to come to the aid of their country. This is just a regular paragraph. The quick brown fox jumped over the lazy dog's back. ### Header 3 > This is a blockquote. > > This is the second paragraph in the blockquote. > > ## This is an H2 in a blockquote 

Resultado:

 <h1>A First Level Header</h1> <h2>A Second Level Header</h2> <p>Now is the time for all good men to come to the aid of their country. This is just a regular paragraph.</p> <p>The quick brown fox jumped over the lazy dog's back.</p> <h3>Header 3</h3> <blockquote> <p>This is a blockquote.</p> <p>This is the second paragraph in the blockquote.</p> <h2>This is an H2 in a blockquote</h2> </blockquote> 

Ênfase na frase

O Markdown usa asteriscos e sublinhados para indicar períodos de ênfase.

Remarcação:

 Some of these words *are emphasized*. Some of these words _are emphasized also_. Use two asterisks for **strong emphasis**. Or, if you prefer, __use two underscores instead__. 

Resultado:

 <p>Some of these words <em>are emphasized</em>. Some of these words <em>are emphasized also</em>.</p> <p>Use two asterisks for <strong>strong emphasis</strong>. Or, if you prefer, <strong>use two underscores instead</strong>.</p> 

Listas

Listas não ordenadas (com marcadores) usam asteriscos, vantagens e hífens ( * , + e - ) como marcadores de lista. Esses três marcadores são intercambiáveis; esta:

 * Candy. * Gum. * Booze. 

esta:

 + Candy. + Gum. + Booze. 

e isto:

 - Candy. - Gum. - Booze. 

todos produzem a mesma saída:

 <ul> <li>Candy.</li> <li>Gum.</li> <li>Booze.</li> </ul> 

As listas ordenadas (numeradas) usam números regulares, seguidos de pontos, como marcadores de lista:

 1. Red 2. Green 3. Blue 

Resultado:

 <ol> <li>Red</li> <li>Green</li> <li>Blue</li> </ol> 

Se você colocar linhas em branco entre os itens, receberá tags <p> para o texto do item da lista. Você pode criar itens de lista com vários parágrafos recuando os parágrafos em 4 espaços ou em uma guia:

 * A list item. With multiple paragraphs. * Another item in the list. 

Resultado:

 <ul> <li><p>A list item.</p> <p>With multiple paragraphs.</p></li> <li><p>Another item in the list.</p></li> </ul> 

Ligações

O Markdown suporta dois estilos para criar links: embutido e referência . Nos dois estilos, você usa colchetes para delimitar o texto que deseja transformar em um link.

Os links de estilo embutido usam parênteses imediatamente após o texto do link. Por exemplo:

 This is an [example link](http://example.com/). 

Resultado:

 <p>This is an <a href="http://example.com/"> example link</a>.</p> 

Opcionalmente, você pode incluir um atributo title entre parênteses:

 This is an [example link](http://example.com/ "With a Title"). 

Resultado:

 <p>This is an <a href="http://example.com/" title="With a Title"> example link</a>.</p> 

Os links no estilo de referência permitem que você faça referência aos seus links por nomes, definidos em outras partes do documento:

 I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3]. [1]: http://google.com/ "Google" [2]: http://search.yahoo.com/ "Yahoo Search" [3]: http://search.msn.com/ "MSN Search" 

Resultado:

 <p>I get 10 times more traffic from <a href="http://google.com/" title="Google">Google</a> than from <a href="http://search.yahoo.com/" title="Yahoo Search">Yahoo</a> or <a href="http://search.msn.com/" title="MSN Search">MSN</a>.</p> 

O atributo title é opcional. Os nomes dos links podem conter letras, números e espaços, mas não diferenciam maiúsculas de minúsculas:

 I start my morning with a cup of coffee and [The New York Times][NY Times]. [ny times]: http://www.nytimes.com/ 

Resultado:

 <p>I start my morning with a cup of coffee and <a href="http://www.nytimes.com/">The New York Times</a>.</p> 

Imagens

A sintaxe da imagem é muito parecida com a sintaxe do link.

Inline (os títulos são opcionais):

 ![alt text](/path/to/img.jpg "Title") 

Estilo de referência:

 ![alt text][id] [id]: /path/to/img.jpg "Title" 

Ambos os exemplos acima produzem a mesma saída:

 <img src="/path/to/img.jpg" alt="alt text" title="Title" /> 

Código

Em um parágrafo regular, você pode criar um intervalo de código envolvendo o texto entre aspas. Quaisquer e comercial ( & ) e colchetes angulares ( < ou > ) serão automaticamente traduzidos em entidades HTML. Isso facilita o uso do Markdown para escrever sobre o código de exemplo HTML:

 I strongly recommend against using any `<blink>` tags. I wish SmartyPants used named entities like `&mdash;` instead of decimal-encoded entites like `&#8212;`. 

Resultado:

 <p>I strongly recommend against using any <code>&lt;blink&gt;</code> tags.</p> <p>I wish SmartyPants used named entities like <code>&amp;mdash;</code> instead of decimal-encoded entites like <code>&amp;#8212;</code>.</p> 

Para especificar um bloco inteiro de código pré-formatado, recue todas as linhas do bloco em 4 espaços ou 1 guia. Assim como nas extensões de código, os caracteres & , < e > serão escapados automaticamente.

Remarcação:

 If you want your page to validate under XHTML 1.0 Strict, you've got to put paragraph tags in your blockquotes: <blockquote> <p>For example.</p> </blockquote> 

Resultado:

 <p>If you want your page to validate under XHTML 1.0 Strict, you've got to put paragraph tags in your blockquotes:</p> <pre><code>&lt;blockquote&gt; &lt;p&gt;For example.&lt;/p&gt; &lt;/blockquote&gt; </code></pre> 

 Markdown: Sintaxe

 
Filosofia

O Markdown deve ser o mais fácil de ler e escrever o mais possível.

A legibilidade, no entanto, é enfatizada acima de tudo. Um documento no formato Markdown deve ser publicado como está, como texto sem formatação, sem parecer ter sido marcado com tags ou instruções de formatação. Embora a sintaxe do Markdown tenha sido influenciada por vários filtros de texto para HTML existentes - incluindo Setext , atx , Textile , reStructuredText , Grutatext e EtText - a maior fonte de inspiração para a sintaxe do Markdown é o formato de email em texto sem formatação.

Para esse fim, a sintaxe de Markdown é composta inteiramente de caracteres de pontuação, caracteres de pontuação que foram cuidadosamente escolhidos para parecer com o que eles significam. Por exemplo, asteriscos em torno de uma palavra realmente se parecem com * ênfase *. Listas de remarcação parecem, bem, listas. Até as citações em bloco parecem passagens de texto citadas, supondo que você já tenha usado o email.
HTML embutido

A sintaxe do Markdown tem uma finalidade: ser usada como um formato para escrever para a web.

Markdown não é um substituto para o HTML, ou mesmo próximo a ele. Sua sintaxe é muito pequena, correspondendo apenas a um subconjunto muito pequeno de tags HTML. A idéia não é criar uma sintaxe que facilite a inserção de tags HTML. Na minha opinião, as tags HTML já são fáceis de inserir. A idéia do Markdown é facilitar a leitura, gravação e edição da prosa. HTML é um formato de publicação ; Markdown é um formato de escrita . Portanto, a sintaxe de formatação do Markdown trata apenas de problemas que podem ser transmitidos em texto sem formatação.

Para qualquer marcação que não seja coberta pela sintaxe do Markdown, basta usar o próprio HTML. Não há necessidade de precedê-lo ou delimitá-lo para indicar que você está mudando do Markdown para o HTML; você acabou de usar as tags.

As únicas restrições são que os elementos HTML no nível do bloco - por exemplo, <div> , <table> , <pre> , <p> etc. - devem ser separados do conteúdo circundante por linhas em branco e as tags de início e fim do bloco não deve ser recuado com tabulações ou espaços. O Markdown é inteligente o suficiente para não adicionar tags <p> extras (indesejadas) em torno das tags em nível de bloco HTML.

Por exemplo, para adicionar uma tabela HTML a um artigo do Markdown:

 This is a regular paragraph. <table> <tr> <td>Foo</td> </tr> </table> This is another regular paragraph. 

Observe que a sintaxe de formatação do Markdown não é processada nas tags HTML no nível do bloco. Por exemplo, você não pode usar o *emphasis* no estilo Markdown dentro de um bloco HTML.

Tags HTML no nível de <span> - por exemplo, <span> , <cite> ou <del> - podem ser usadas em qualquer lugar do parágrafo, item da lista ou cabeçalho do Markdown. Se desejar, você pode até usar tags HTML em vez da formatação Markdown; por exemplo, se você preferir usar as tags HTML <a> ou <img> vez da sintaxe do link ou da imagem do Markdown, vá em frente.

Diferentemente das tags HTML em nível de bloco, a sintaxe do Markdown é processada nas tags em nível de extensão.
Escapamento automático para caracteres especiais

No HTML, existem dois caracteres que exigem tratamento especial:

 '< '  e  '& '. Colchetes de ângulo esquerdo são usados ​​para iniciar as tags; e comercial são usados ​​para denotar entidades HTML. Se você deseja usá-los como caracteres literais, deve escapar deles como entidades, por exemplo, &lt; e &amp; .


E comercial, em particular, é um problema para os autores da web. Se você quiser escrever sobre 'AT&T', você precisa escrever ' AT&amp;T '. Você ainda precisa escapar do e comercial nos URLs. Portanto, se você deseja vincular a:

 http://images.google.com/images?num=30&q=larry+bird 

você precisa codificar o URL como:

http://images.google.com/images?num=30&amp;q=larry+bird 

no atributo href tag de âncora. Escusado será dizer que isso é fácil de esquecer e provavelmente é a fonte mais comum de erros de validação de HTML em sites de outra forma bem marcados.

O Markdown permite que você use esses personagens naturalmente, cuidando de todos os escapamentos necessários para você. Se você usar um e comercial como parte de uma entidade HTML, ele permanecerá inalterado; caso contrário, será traduzido para o &amp; .

Portanto, se você deseja incluir um símbolo de direitos autorais em seu artigo, escreva:

 &copy; 

e Markdown o deixará em paz. Mas se você escrever:

 AT&T 

O Markdown o traduzirá para:

 AT&amp;T 

Da mesma forma, como o Markdown suporta HTML embutido , se você usar colchetes angulares como delimitadores para tags HTML, o Markdown os tratará como tal. Mas se você escrever:

 4 < 5 

O Markdown o traduzirá para:

 4 &lt; 5 

No entanto, dentro dos intervalos e blocos do código Markdown, colchetes angulares e e comercial são sempre codificados automaticamente. Isso facilita o uso do Markdown para escrever sobre o código HTML. (Ao contrário do HTML bruto, que é um formato terrível para escrever sobre sintaxe HTML, porque todos os códigos < e & no seu exemplo de exemplo precisam ser escapados.)
Elementos do bloco
Parágrafos e quebras de linha

Um parágrafo é simplesmente uma ou mais linhas consecutivas de texto, separadas por uma ou mais linhas em branco. (Uma linha em branco é qualquer linha que se parece com uma linha em branco - uma linha que não contém nada além de espaços ou tabulações é considerada em branco.) Parágrafos normais não devem ser recuados com espaços ou tabulações.

A implicação da regra "uma ou mais linhas consecutivas de texto" é que o Markdown suporta parágrafos de texto "embutidos". Isso difere significativamente da maioria dos outros formatadores de texto para HTML (incluindo a opção "Converter quebras de linha" do Movable Type) que traduz todos os caracteres de quebra de linha de um parágrafo em uma tag <br /> .

Quando você deseja inserir uma tag de interrupção <br /> usando o Markdown, finaliza uma linha com dois ou mais espaços e digita return.

Sim, é preciso um pouco mais de esforço para criar um <br /> , mas uma regra simplista de "toda quebra de linha é <br /> " não funcionaria para o Markdown. Os itens de cotação em bloco e de vários parágrafos no estilo de email do Markdown funcionam melhor - e ficam melhores - quando você os formata com pausas duras.
Cabeçalhos

O Markdown suporta dois estilos de cabeçalhos, Setext e atx .

Os cabeçalhos no estilo Setext são "sublinhados" usando sinais de igual (para cabeçalhos de primeiro nível) e traços (para cabeçalhos de segundo nível). Por exemplo:

 This is an H1 ============= This is an H2 ------------- 

Qualquer número de = ou s sublinhados funcionará.

Os cabeçalhos no estilo Atx usam 1-6 caracteres hash no início da linha, correspondendo aos níveis de cabeçalho 1-6. Por exemplo:

 # This is an H1 ## This is an H2 ###### This is an H6 

Opcionalmente, você pode "fechar" cabeçalhos no estilo atx. Isso é puramente cosmético - você pode usá-lo se achar melhor. Os hashes de fechamento nem precisam corresponder ao número de hashes usados ​​para abrir o cabeçalho. (O número de hashes de abertura determina o nível do cabeçalho.):

 # This is an H1 # ## This is an H2 ## ### This is an H3 ###### 

Citações em bloco

O Markdown usa caracteres no estilo de email > para cotações em bloco. Se você está familiarizado com a citação de passagens de texto em uma mensagem de e-mail, sabe como criar uma citação em bloco no Markdown. Parece melhor se você envolver o texto com força e colocar um > antes de cada linha:

 > This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet, > consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus. > Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus. > > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse > id sem consectetuer libero luctus adipiscing. 

O Markdown permite que você seja preguiçoso e coloque apenas o > antes da primeira linha de um parágrafo rígido:

 > This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus. > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse id sem consectetuer libero luctus adipiscing. 

As cotações em bloco podem ser aninhadas (ou seja, uma cotação em bloco) adicionando níveis adicionais de > :

 > This is the first level of quoting. > > > This is nested blockquote. > > Back to the first level. 

As citações de bloco podem conter outros elementos de Markdown, incluindo cabeçalhos, listas e blocos de código:

 > ## This is a header. > > 1. This is the first list item. > 2. This is the second list item. > > Here's some example code: > > return shell_exec("echo $input | $markdown_script"); 

Qualquer editor de texto decente deve facilitar a cotação no estilo de email. Por exemplo, com o BBEdit, você pode fazer uma seleção e escolher Aumentar nível de cotação no menu Texto.
Listas

O Markdown suporta listas ordenadas (numeradas) e não ordenadas (com marcadores).

As listas não ordenadas usam asteriscos, vantagens e hífens - de forma intercambiável - como marcadores de lista:

 * Red * Green * Blue 

é equivalente a:

 + Red + Green + Blue 

e:

 - Red - Green - Blue 

As listas ordenadas usam números seguidos de pontos:

 1. Bird 2. McHale 3. Parish 

É importante observar que os números reais que você usa para marcar a lista não têm efeito na saída HTML que o Markdown produz. O HTML Markdown produzido a partir da lista acima é:

 <ol> <li>Bird</li> <li>McHale</li> <li>Parish</li> </ol> 

Se você escreveu a lista no Markdown assim:

 1. Bird 1. McHale 1. Parish 

ou até:

 3. Bird 1. McHale 8. Parish 

você obteria exatamente a mesma saída HTML. A questão é que, se você quiser, pode usar números ordinais nas listas de Markdown ordenadas, para que os números na sua fonte correspondam aos números no HTML publicado. Mas se você quer ser preguiçoso, não precisa.

Se você usar a numeração de lista lenta, no entanto, ainda deverá iniciar a lista com o número 1. Em algum momento no futuro, o Markdown poderá suportar o início de listas ordenadas em um número arbitrário.

Os marcadores de lista geralmente começam na margem esquerda, mas podem ser recuados em até três espaços. Os marcadores de lista devem ser seguidos por um ou mais espaços ou uma guia.

Para fazer com que as listas tenham uma boa aparência, você pode agrupar itens com recuos pendurados:

 * Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus. * Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse id sem consectetuer libero luctus adipiscing. 

Mas se você quer ser preguiçoso, não precisa:

 * Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus. * Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse id sem consectetuer libero luctus adipiscing. 

Se os itens da lista forem separados por linhas em branco, o Markdown agrupará os itens nas tags <p> na saída HTML. Por exemplo, esta entrada:

 * Bird * Magic 

vai se transformar em:

 <ul> <li>Bird</li> <li>Magic</li> </ul> 

Mas isso:

 * Bird * Magic 

vai se transformar em:

 <ul> <li><p>Bird</p></li> <li><p>Magic</p></li> </ul> 



[GITHUB]: https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet


[GITHUB]: https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf








