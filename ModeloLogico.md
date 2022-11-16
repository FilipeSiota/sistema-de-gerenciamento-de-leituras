# Modelo Lógico do Banco de Dados

- Usuario(<u>id</u>, nome, email, usuario, senha)
- Editora(<u>id</u>, nome site, email, nacionalidade)
- Editora_Telefone(<u>id</u>, numero, editora_id)
    - _editora_id referencia Editora_
- Colecao(<u>id</u>, nome)
- Genero(<u>id</u>, nome, descricao)
- Autor(<u>id</u>, nome, naturalidade, biografia)
- Livro(<u>id</u>, nome, edicao, ano, idioma, sinopse, quant_paginas, editora_id, colecao_id)
    - _editora_id referencia Editora_
    - _colecao_id referencia Colecao_
- Livro_Genero(<u>livro_id</u>, <u>genero_id</u>)
    - _livro_id referencia Livro_
    - _genero_id referencia Genero_
- Livro_Autor(<u>livro_id</u>, <u>autor_id</u>)
    - _livro_id referencia Livro_
    - _autor_id referencia Autor_
- Progresso_Leitura(<u>usuario_id</u>, <u>livro_id</u>, pagina_atual, status)
    - _usuario_id referencia Usuario_
    - _livro_id referencia Livro_