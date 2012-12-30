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
    <dt><strong>página 79: </strong></dt>
    <dd>
        A view de deleção está incorreta, ela repete a view de update o correto é usar::
        <ul>
            <li>
                <strong>sample1/app/views/tasks/destroy.js.erb</strong>
<pre>
$("div#dialogFrame").remove();
$("section table tbody").children().remove();
$("section table tbody").append("&lt;%= j render @tasks %&gt;");
</pre>
            </li>
        </ul>
    </dd>
</dl>
