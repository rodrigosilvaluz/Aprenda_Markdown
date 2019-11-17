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

    Captura de tela do menu Movable Type 'Text Formatting'

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


