task_manager
============

Task Manager App (sample1)

Projeto de acompanhamento do Livro:

Ruby on Rails - Desenvolvimento Fácil e Rápido de Aplicações Web

http://www.novatec.com.br/livros/rubyonrails2/

Alguns erros de código corrigidos:

página 73:
  javascript render recebe o parametro de layout incorreto o que impede a abertura do dialog:
  
  ao invéz de:
    $("<div/>").attr("id", "dialogFrame").append($("<%= j render file: 'tasks/edit.html.erb', layout: false %>")).dialog({autoOpen: true});
  usear:
    $("<div/>").attr("id", "dialogFrame").append($("<%= j render file: 'tasks/edit.html.erb', layout: nil %>")).dialog({autoOpen: true});
    
  isso vale para create.js.erb e para update.js.erb
