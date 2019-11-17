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

Os itens da lista podem consistir em vários parágrafos. Cada parágrafo subsequente em um item da lista deve ser recuado por 4 espaços ou uma guia:

 1. This is a list item with two paragraphs. Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus. Donec sit amet nisl. Aliquam semper ipsum sit amet velit. 2. Suspendisse id sem consectetuer libero luctus adipiscing. 

Parece bom se você recuar todas as linhas dos parágrafos subsequentes, mas aqui novamente, o Markdown permitirá que você seja preguiçoso:

 * This is a list item with two paragraphs. This is the second paragraph in the list item. You're only required to indent the first line. Lorem ipsum dolor sit amet, consectetuer adipiscing elit. * Another item in the same list. 

Para colocar uma citação em bloco em um item da lista, os delimitadores da citação em bloco precisam ser recuados:

 * A list item with a blockquote: > This is a blockquote > inside a list item. 

Para colocar um bloco de código em um item da lista, o bloco de código precisa ser recuado duas vezes - 8 espaços ou duas guias:

 * A list item with a code block: <code goes here> 

Vale a pena notar que é possível acionar uma lista ordenada por acidente, escrevendo algo como isto:

 1986. What a great season. 

Em outras palavras, uma sequência numérica-período-espaço no início de uma linha. Para evitar isso, você pode escapar com barra invertida do período:

 1986\. What a great season. 

Blocos de código

Blocos de código pré-formatados são usados ​​para escrever sobre código-fonte de programação ou marcação. Em vez de formar parágrafos normais, as linhas de um bloco de código são interpretadas literalmente. O Markdown agrupa um bloco de código nas tags <pre> e <code> .

Para produzir um bloco de código no Markdown, basta recuar todas as linhas do bloco em pelo menos 4 espaços ou 1 guia. Por exemplo, dada esta entrada:

 This is a normal paragraph: This is a code block. 

A remarcação gerará:

 <p>This is a normal paragraph:</p> <pre><code>This is a code block. </code></pre> 

Um nível de recuo - 4 espaços ou 1 guia - é removido de cada linha do bloco de código. Por exemplo, isto:

 Here is an example of AppleScript: tell application "Foo" beep end tell 

vai se transformar em:

 <p>Here is an example of AppleScript:</p> <pre><code>tell application "Foo" beep end tell </code></pre> 

Um bloco de código continua até atingir uma linha que não é recuada (ou no final do artigo).

Dentro de um bloco de código, e comercial ( & ) e colchetes angulares ( < e > ) são convertidos automaticamente em entidades HTML. Isso facilita muito a inclusão de exemplos de código-fonte HTML usando o Markdown - basta colá-lo e recuá-lo, e o Markdown lidará com o incômodo de codificar os e comercial e colchetes angulares. Por exemplo, isto:

  <div class="footer"> &copy; 2004 Foo Corporation </div> 

vai se transformar em:

 <pre><code>&lt;div class="footer"&gt; &amp;copy; 2004 Foo Corporation &lt;/div&gt; </code></pre> 

A sintaxe regular do Markdown não é processada nos blocos de código. Por exemplo, asteriscos são apenas literais dentro de um bloco de código. Isso significa que também é fácil usar o Markdown para escrever sobre a própria sintaxe do Markdown.
Regras horizontais

Você pode produzir uma tag de regra horizontal ( <hr /> ) colocando três ou mais hífens, asteriscos ou sublinhados em uma linha por si mesmos. Se desejar, você pode usar espaços entre os hífens ou asteriscos. Cada uma das seguintes linhas produzirá uma regra horizontal:

 * * * *** ***** - - - --------------------------------------- 

Elementos de extensão
Ligações

O Markdown suporta dois estilos de links: embutido e referência .

Nos dois estilos, o texto do link é delimitado por [colchetes].

Para criar um link embutido, use um conjunto de parênteses regulares imediatamente após o colchete de fechamento do texto do link. Dentro dos parênteses, coloque o URL para o qual deseja apontar o link, juntamente com um título opcional para o link, entre aspas. Por exemplo:

 This is [an example](http://example.com/ "Title") inline link. [This link](http://example.net/) has no title attribute. 

Vai produzir:

 <p>This is <a href="http://example.com/" title="Title"> an example</a> inline link.</p> <p><a href="http://example.net/">This link</a> has no title attribute.</p> 

Se você estiver se referindo a um recurso local no mesmo servidor, poderá usar caminhos relativos:

 See my [About](/about/) page for details. 

Os links no estilo de referência usam um segundo conjunto de colchetes, dentro do qual você coloca um rótulo de sua escolha para identificar o link:

 This is [an example][id] reference-style link. 

Opcionalmente, você pode usar um espaço para separar os conjuntos de colchetes:

 This is [an example] [id] reference-style link. 

Então, em qualquer lugar do documento, você define o rótulo do seu link assim, em uma linha por si só:

 [id]: http://example.com/ "Optional Title Here" 

Isso é:

    Colchetes contendo o identificador do link (opcionalmente recuado da margem esquerda usando até três espaços);
    seguido por dois pontos;
    seguido por um ou mais espaços (ou tabulações);
    seguido pelo URL do link;
    opcionalmente seguido por um atributo title para o link, entre aspas duplas ou simples ou entre parênteses. 

As três definições de link a seguir são equivalentes:

 [foo]: http://example.com/ "Optional Title Here" [foo]: http://example.com/ 'Optional Title Here' [foo]: http://example.com/ (Optional Title Here) 

Nota: Há um bug conhecido no Markdown.pl 1.0.1 que impede que aspas simples sejam usadas para delimitar títulos de links.

O URL do link pode, opcionalmente, estar entre colchetes angulares:

 [id]: <http://example.com/> "Optional Title Here" 

Você pode colocar o atributo title na próxima linha e usar espaços ou guias extras para preenchimento, que tendem a parecer melhor com URLs mais longos:

 [id]: http://example.com/longish/path/to/resource/here "Optional Title Here" 

As definições de link são usadas apenas para criar links durante o processamento do Markdown e são retiradas do documento na saída HTML.

Os nomes de definição de link podem consistir em letras, números, espaços e pontuação - mas não diferenciam maiúsculas de minúsculas. Por exemplo, esses dois links:

 [link text][a] [link text][A] 

são equivalentes.

O atalho implícito do nome do link permite omitir o nome do link; nesse caso, o próprio texto do link é usado como o nome. Basta usar um conjunto vazio de colchetes - por exemplo, para vincular a palavra "Google" ao site google.com, você pode simplesmente escrever:

 [Google][] 

E então defina o link:

 [Google]: http://google.com/ 

Como os nomes dos links podem conter espaços, esse atalho funciona até para várias palavras no texto do link:

 Visit [Daring Fireball][] for more information. 

E então defina o link:

 [Daring Fireball]: http://daringfireball.net/ 

As definições de link podem ser colocadas em qualquer lugar do seu documento Markdown. Costumo colocá-los imediatamente após cada parágrafo em que são usados, mas se você quiser, pode colocá-los todos no final do documento, como notas de rodapé.

Aqui está um exemplo de links de referência em ação:

 I get 10 times more traffic from [Google] [1] than from [Yahoo] [2] or [MSN] [3]. [1]: http://google.com/ "Google" [2]: http://search.yahoo.com/ "Yahoo Search" [3]: http://search.msn.com/ "MSN Search" 

Usando o atalho implícito do nome do link, você pode escrever:

 I get 10 times more traffic from [Google][] than from [Yahoo][] or [MSN][]. [google]: http://google.com/ "Google" [yahoo]: http://search.yahoo.com/ "Yahoo Search" [msn]: http://search.msn.com/ "MSN Search" 

Ambos os exemplos acima produzirão a seguinte saída HTML:

 <p>I get 10 times more traffic from <a href="http://google.com/" title="Google">Google</a> than from <a href="http://search.yahoo.com/" title="Yahoo Search">Yahoo</a> or <a href="http://search.msn.com/" title="MSN Search">MSN</a>.</p> 

Para comparação, aqui está o mesmo parágrafo escrito usando o estilo de link embutido do Markdown:

 I get 10 times more traffic from [Google](http://google.com/ "Google") than from [Yahoo](http://search.yahoo.com/ "Yahoo Search") or [MSN](http://search.msn.com/ "MSN Search"). 

O ponto dos links no estilo de referência não é que eles sejam mais fáceis de escrever. O ponto é que, com links no estilo de referência, a fonte do documento é muito mais legível. Compare os exemplos acima: usando links de estilo de referência, o parágrafo em si tem apenas 81 caracteres; com links de estilo embutido, são 176 caracteres; e como HTML bruto, são 234 caracteres. No HTML bruto, há mais marcação do que texto.

Com os links no estilo de referência do Markdown, um documento de origem se assemelha muito mais à saída final, conforme renderizada em um navegador. Ao permitir que você mova os metadados relacionados à marcação para fora do parágrafo, você pode adicionar links sem interromper o fluxo narrativo da sua prosa.
Ênfase

O markdown trata os asteriscos ( * ) e sublinhados ( _ ) como indicadores de ênfase. O texto quebrado com um * ou _ será quebrado com uma tag HTML <em> ; double * ou _ serão envoltos por uma tag HTML <strong> . Por exemplo, esta entrada:

 *single asterisks* _single underscores_ **double asterisks** __double underscores__ 

vai produzir:

 <em>single asterisks</em> <em>single underscores</em> <strong>double asterisks</strong> <strong>double underscores</strong> 

Você pode usar o estilo que preferir; a única restrição é que o mesmo caractere deve ser usado para abrir e fechar um período de ênfase.

A ênfase pode ser usada no meio de uma palavra:

 un*frigging*believable 

Mas se você colocar um * ou _ com espaços, ele será tratado como um asterisco ou sublinhado literal.

Para produzir um asterisco literal ou sublinhado em uma posição em que, de outra forma, seria usado como um delimitador de ênfase, você pode escapar da barra invertida:

 \*this text is surrounded by literal asterisks\* 

Código

Para indicar um intervalo de código, envolva-o com aspas ( ` ). Diferentemente de um bloco de código pré-formatado, uma extensão de código indica o código dentro de um parágrafo normal. Por exemplo:

 Use the `printf()` function. 

vai produzir:

 <p>Use the <code>printf()</code> function.</p> 

Para incluir um caractere de backtick literal em um período de código, você pode usar vários backticks como delimitadores de abertura e fechamento:

 ``There is a literal backtick (`) here.`` 

que produzirá isso:

 <p><code>There is a literal backtick (`) here.</code></p> 

Os delimitadores de backtick em torno de uma extensão de código podem incluir espaços - um após a abertura, um antes do fechamento. Isso permite que você coloque caracteres literais de backtick no início ou no final de um período de código:

 A single backtick in a code span: `` ` `` A backtick-delimited string in a code span: `` `foo` `` 

vai produzir:

 <p>A single backtick in a code span: <code>`</code></p> <p>A backtick-delimited string in a code span: <code>`foo`</code></p> 

Com um intervalo de código, e comercial e colchetes angulares são codificados como entidades HTML automaticamente, o que facilita a inclusão de exemplo de tags HTML. Markdown irá transformar isso:

 Please don't use any `<blink>` tags. 

para dentro:

 <p>Please don't use any <code>&lt;blink&gt;</code> tags.</p> 

Você pode escrever isto:

 `&#8212;` is the decimal-encoded equivalent of `&mdash;`. 

para produzir:

 <p><code>&amp;#8212;</code> is the decimal-encoded equivalent of <code>&amp;mdash;</code>.</p> 

Imagens

É certo que é bastante difícil criar uma sintaxe "natural" para colocar imagens em um formato de documento de texto sem formatação.

O Markdown usa uma sintaxe de imagem que se parece com a sintaxe dos links, permitindo dois estilos: inline e referência .

A sintaxe da imagem embutida é assim:

 ![Alt text](/path/to/img.jpg) ![Alt text](/path/to/img.jpg "Optional title") 

Isso é:

    Um ponto de exclamação:! ;
    seguido por um conjunto de colchetes, contendo o texto do atributo alt para a imagem;
    seguido por um conjunto de parênteses, contendo o URL ou o caminho para a imagem e um atributo de title opcional entre aspas duplas ou simples. 

A sintaxe da imagem no estilo de referência tem a seguinte aparência:

 ![Alt text][id] 

Onde "id" é o nome de uma referência de imagem definida. As referências de imagem são definidas usando uma sintaxe idêntica às referências de link:

 [id]: url/to/image "Optional title attribute" 

No momento da redação deste artigo, o Markdown não possui sintaxe para especificar as dimensões de uma imagem; se isso for importante para você, você pode simplesmente usar tags HTML <img> regulares.
Diversos
Links automáticos

O Markdown suporta um estilo de atalho para criar links "automáticos" para URLs e endereços de email: basta colocar o URL ou o endereço de email entre colchetes angulares. O que isso significa é que, se você deseja mostrar o texto real de um URL ou endereço de e-mail e também tem um link clicável, é possível:

 <http://example.com/> 

O Markdown transformará isso em:

 <a href="http://example.com/">http://example.com/</a> 

Os links automáticos para endereços de email funcionam da mesma maneira, exceto que o Markdown também executará um pouco de codificação decimal e hexadecimal aleatória de entidades para ajudar a ocultar seu endereço de spambots de coleta de endereços. Por exemplo, o Markdown transformará isso:

 < address@example.com > 

em algo como isto:

 <a href="&#x6D;&#x61;i&#x6C;&#x74;&#x6F;:&#x61;&#x64;&#x64;&#x72;&#x65; &#115;&#115;&#64;&#101;&#120;&#x61;&#109;&#x70;&#x6C;e&#x2E;&#99;&#111; &#109;">&#x61;&#x64;&#x64;&#x72;&#x65;&#115;&#115;&#64;&#101;&#120;&#x61; &#109;&#x70;&#x6C;e&#x2E;&#99;&#111;&#109;</a> 

que será renderizado em um navegador como um link clicável para " address@example.com ".

(Esse tipo de truque de codificação de entidade realmente engana muitos, se não a maioria, bots de coleta de endereços, mas definitivamente não engana todos eles. É melhor que nada, mas um endereço publicado dessa maneira provavelmente acabará por receber Spam.)
Escapes de barra invertida

O Markdown permite que você use escapes de barra invertida para gerar caracteres literais que, de outra forma, teriam um significado especial na sintaxe de formatação do Markdown. Por exemplo, se você quiser colocar uma palavra entre asteriscos literais (em vez de uma tag HTML <em> ), poderá usar barras invertidas antes dos asteriscos, assim:

 \*literal asterisks\* 

O Markdown fornece escapes de barra invertida para os seguintes caracteres:

 \ backslash ` backtick * asterisk _ underscore {} curly braces [] square brackets () parentheses # hash mark + plus sign - minus sign (hyphen) . dot ! exclamation mark 






[GITHUB]: https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet

Markdown Cheatsheet
Adam Pritchard edited this page on May 29, 2017 · 96 revisions

This is intended as a quick reference and showcase. For more complete info, see John Gruber's original spec and the Github-flavored Markdown info page.

Note that there is also a Cheatsheet specific to Markdown Here if that's what you're looking for. You can also check out more Markdown tools.
Table of Contents


# H1
## H2
### H3
#### H4
##### H5
###### H6

Alternatively, for H1 and H2, an underline-ish style:

Alt-H1
======

Alt-H2
------

H1
H2
H3
H4
H5
H6

Alternatively, for H1 and H2, an underline-ish style:
Alt-H1
Alt-H2
Emphasis

Emphasis, aka italics, with *asterisks* or _underscores_.

Strong emphasis, aka bold, with **asterisks** or __underscores__.

Combined emphasis with **asterisks and _underscores_**.

Strikethrough uses two tildes. ~~Scratch this.~~

Emphasis, aka italics, with asterisks or underscores.

Strong emphasis, aka bold, with asterisks or underscores.

Combined emphasis with asterisks and underscores.

Strikethrough uses two tildes. Scratch this.
Lists

(In this example, leading and trailing spaces are shown with with dots: ⋅)

1. First ordered list item
2. Another item
⋅⋅* Unordered sub-list. 
1. Actual numbers don't matter, just that it's a number
⋅⋅1. Ordered sub-list
4. And another item.

⋅⋅⋅You can have properly indented paragraphs within list items. Notice the blank line above, and the leading spaces (at least one, but we'll use three here to also align the raw Markdown).

⋅⋅⋅To have a line break without a paragraph, you will need to use two trailing spaces.⋅⋅
⋅⋅⋅Note that this line is separate, but within the same paragraph.⋅⋅
⋅⋅⋅(This is contrary to the typical GFM line break behaviour, where trailing spaces are not required.)

* Unordered list can use asterisks
- Or minuses
+ Or pluses

    First ordered list item
    Another item

    Unordered sub-list.

    Actual numbers don't matter, just that it's a number

    Ordered sub-list

    And another item.

    You can have properly indented paragraphs within list items. Notice the blank line above, and the leading spaces (at least one, but we'll use three here to also align the raw Markdown).

    To have a line break without a paragraph, you will need to use two trailing spaces.
    Note that this line is separate, but within the same paragraph.
    (This is contrary to the typical GFM line break behaviour, where trailing spaces are not required.)

    Unordered list can use asterisks

    Or minuses

    Or pluses

Links

There are two ways to create links.

[I'm an inline-style link](https://www.google.com)

[I'm an inline-style link with title](https://www.google.com "Google's Homepage")

[I'm a reference-style link][Arbitrary case-insensitive reference text]

[I'm a relative reference to a repository file](../blob/master/LICENSE)

[You can use numbers for reference-style link definitions][1]

Or leave it empty and use the [link text itself].

URLs and URLs in angle brackets will automatically get turned into links. 
http://www.example.com or <http://www.example.com> and sometimes 
example.com (but not on Github, for example).

Some text to show that the reference links can follow later.

[arbitrary case-insensitive reference text]: https://www.mozilla.org
[1]: http://slashdot.org
[link text itself]: http://www.reddit.com

I'm an inline-style link

I'm an inline-style link with title

I'm a reference-style link

I'm a relative reference to a repository file

You can use numbers for reference-style link definitions

Or leave it empty and use the link text itself.

URLs and URLs in angle brackets will automatically get turned into links. http://www.example.com or http://www.example.com and sometimes example.com (but not on Github, for example).

Some text to show that the reference links can follow later.
Images

Here's our logo (hover to see the title text):

Inline-style: 
![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 1")

Reference-style: 
![alt text][logo]

[logo]: https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 2"

Here's our logo (hover to see the title text):

Inline-style: alt text

Reference-style: alt text
Code and Syntax Highlighting

Code blocks are part of the Markdown spec, but syntax highlighting isn't. However, many renderers -- like Github's and Markdown Here -- support syntax highlighting. Which languages are supported and how those language names should be written will vary from renderer to renderer. Markdown Here supports highlighting for dozens of languages (and not-really-languages, like diffs and HTTP headers); to see the complete list, and how to write the language names, see the highlight.js demo page.

Inline `code` has `back-ticks around` it.

Inline code has back-ticks around it.

Blocks of code are either fenced by lines with three back-ticks ```, or are indented with four spaces. I recommend only using the fenced code blocks -- they're easier and only they support syntax highlighting.

```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```
 
```python
s = "Python syntax highlighting"
print s
```
 
```
No language indicated, so no syntax highlighting. 
But let's throw in a <b>tag</b>.
```

var s = "JavaScript syntax highlighting";
alert(s);

s = "Python syntax highlighting"
print s

No language indicated, so no syntax highlighting in Markdown Here (varies on Github). 
But let's throw in a <b>tag</b>.

Tables

Tables aren't part of the core Markdown spec, but they are part of GFM and Markdown Here supports them. They are an easy way of adding tables to your email -- a task that would otherwise require copy-pasting from another application.

Colons can be used to align columns.

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

There must be at least 3 dashes separating each header cell.
The outer pipes (|) are optional, and you don't need to make the 
raw Markdown line up prettily. You can also use inline Markdown.

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3

Colons can be used to align columns.
Tables 	Are 	Cool
col 3 is 	right-aligned 	$1600
col 2 is 	centered 	$12
zebra stripes 	are neat 	$1

There must be at least 3 dashes separating each header cell. The outer pipes (|) are optional, and you don't need to make the raw Markdown line up prettily. You can also use inline Markdown.
Markdown 	Less 	Pretty
Still 	renders 	nicely
1 	2 	3
Blockquotes

> Blockquotes are very handy in email to emulate reply text.
> This line is part of the same quote.

Quote break.

> This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can *put* **Markdown** into a blockquote. 

    Blockquotes are very handy in email to emulate reply text. This line is part of the same quote.

Quote break.

    This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can put Markdown into a blockquote.

Inline HTML

You can also use raw HTML in your Markdown, and it'll mostly work pretty well.

<dl>
  <dt>Definition list</dt>
  <dd>Is something people use sometimes.</dd>

  <dt>Markdown in HTML</dt>
  <dd>Does *not* work **very** well. Use HTML <em>tags</em>.</dd>
</dl>

Definition list
    Is something people use sometimes.
Markdown in HTML
    Does *not* work **very** well. Use HTML tags.

Horizontal Rule

Three or more...

---

Hyphens

***

Asterisks

___

Underscores

Three or more...

Hyphens

Asterisks

Underscores
Line Breaks

My basic recommendation for learning how line breaks work is to experiment and discover -- hit <Enter> once (i.e., insert one newline), then hit it twice (i.e., insert two newlines), see what happens. You'll soon learn to get what you want. "Markdown Toggle" is your friend.

Here are some things to try out:

Here's a line for us to start with.

This line is separated from the one above by two newlines, so it will be a *separate paragraph*.

This line is also a separate paragraph, but...
This line is only separated by a single newline, so it's a separate line in the *same paragraph*.

Here's a line for us to start with.

This line is separated from the one above by two newlines, so it will be a separate paragraph.

This line is also begins a separate paragraph, but...
This line is only separated by a single newline, so it's a separate line in the same paragraph.

(Technical note: Markdown Here uses GFM line breaks, so there's no need to use MD's two-space line breaks.)
YouTube Videos

They can't be added directly but you can add an image with a link to the video like this:

<a href="http://www.youtube.com/watch?feature=player_embedded&v=YOUTUBE_VIDEO_ID_HERE
" target="_blank"><img src="http://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg" 
alt="IMAGE ALT TEXT HERE" width="240" height="180" border="10" /></a>

Or, in pure Markdown, but losing the image sizing and border:

[![IMAGE ALT TEXT HERE](http://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg)](http://www.youtube.com/watch?v=YOUTUBE_VIDEO_ID_HERE)

Referencing a bug by #bugID in your git commit links it to the slip. For example #1.https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet


[GITHUB]: https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf








