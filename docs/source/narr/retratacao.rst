﻿.. _retratacao:

Retratação
==========

Como regra, arquivos do tipo retratação e retratação parcial devem apresentar o valor `retraction` ou `partial-retraction` no atributo `@article-type`. O texto do elemento `//subj-group[@subj-group-type="heading"]/subject` deve conter a seção apresentada no sumário do número e, no elemento :ref:`elemento-article-title`, a informação deve ser `ARTIGO RETRATADO` (pt), `RETRACTED ARTICLE` (en) `ARTÍCULO RETRACTADO` (es), entre colchetes, mais dois pontos e o título do artigo.
 
O elemento :ref:`elemento-related-article` é utilizado para referenciar o artigo que se deseja retratar. Esta tag terá o valor `retracted-article` ou  `partial-retraction`. O `ext-link-type` sempre será do tipo `doi` e `xlink:href` o número de DOI do artigo que está sendo retratado.
 
A seção deve ser considerada tal qual no PDF, normalmente “Retratação” (pt), “Retraction” (en), ou “Retractación” (es).
 
Exemplo:
 
.. code-block:: xml

    <article article-type="retraction" specific-use="sps-1.6" dtd-version="1.0" xml:lang="en" xmlns:xlink="http://www.w3.org/1999/xlink">
     	<front>
        ...
       <article-meta>
            	<article-id pub-id-type="doi">DOI (PRÓPRIO retirar) DA RETRATAÇÃO</article-id>
            		<article-categories>
                			<subj-group subj-group-type="heading">
                    			<subject>Retratação</subject>
                			</subj-group>
                			...
            		</article-categories>
            	<title-group>
                		<article-title>[ARTIGO RETRATADO]: título do artigo retratado</article-title>
            	</title-group>
            	...
         	 	</permissions>
            		<related-article related-article-type="retracted-article" id="ra1" xlink:href="10.1590/abd1806-4841.20142998" ext-link-type="doi"/>
     	...
     	</front>
     	<body>
         		<p>Texto da Retratação</p>
          </body>
     	...
     </article>
 
 
.. note:: :ref:`elemento-related-article` deve ser inserido abaixo das informações de :ref:`elemento-permissions` ou acima de :ref:`elemento-counts`.

O XML do artigo retratado ou parcialmente retratado é alterado pela equipe SciELO. Para mais informações, leia o `Guia para o registro e publicação de retratação <http://www.scielo.org/local/File/Guia%20para%20o%20registro%20e%20publica%C3%A7%C3%A3o%20de%20retrata%C3%A7%C3%A3o.pdf>`_.


.. {"reviewed_on": "20170829", "by": "carolina.tanigushi@scielo.org"}
