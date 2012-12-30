Task Manager
============

Task Manager App (sample1)

Projeto de acompanhamento do Livro:

Ruby on Rails - Desenvolvimento Fácil e Rápido de Aplicações Web

http://www.novatec.com.br/livros/rubyonrails2/

Alguns erros de código corrigidos:

<dl>
<dt><strong>página 73: </strong></dt>
<dd>
javascript render recebe o parametro de layout incorreto o que impede a abertura do dialog:
<ul>
<li>
  <strong>ao invéz de:</strong>
    (...).append($("&lt;%= j render file: 'tasks/edit.html.erb', layout: <strong>false</strong> %&gt;")).(...);
</li>
<li>
  <strong>usar:</strong>
    (...).append($("&lt;%= j render file: 'tasks/edit.html.erb', layout: <strong>nil</strong> %&gt;")).(...);
</li>
</ul>
  isso vale para <stong>create.js.erb</strong> e para <strong>update.js.erb</strong>
</dd>
</dl>
