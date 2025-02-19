<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Documentação da API Flask</title>
    <style>
        body { font-family: Arial, sans-serif; line-height: 1.6; margin: 20px; }
        h1, h2 { color: #333; }
        code { background: #f4f4f4; padding: 5px; border-radius: 5px; }
        pre { background: #f4f4f4; padding: 10px; border-radius: 5px; overflow-x: auto; }
    </style>
</head>
<body>
    <h1>📖 API de Gerenciamento de Livros - Flask</h1>
    <p>Esta API permite gerenciar livros, autores e clientes utilizando Flask. Suporta operações <b>GET, POST, PUT e DELETE</b>.</p>

    <h2>🚀 Como Rodar</h2>
    <pre><code>pip install flask
python app.py</code></pre>

    <h2>📌 Endpoints Disponíveis</h2>

    <h3>🔍 1. Obter Todos os Livros</h3>
    <p><b>Rota:</b> <code>GET /livro</code></p>
    <p><b>Exemplo de Resposta:</b></p>
    <pre><code>{
    "1": {"título": "O Segredo do Vale", "autor_id": "1", "ano_publicacao": 2018, "gênero": "Ficção", "preco": 45.90}
}</code></pre>

    <h3>🔍 2. Obter Todos os Autores</h3>
    <p><b>Rota:</b> <code>GET /autor</code></p>
    <p><b>Exemplo de Resposta:</b></p>
    <pre><code>{
    "1": {"nome": "Clara Mendes", "nacionalidade": "Brasileira", "ano_nascimento": 1980, "obras_notáveis": ["O Segredo do Vale", "Noites de Verão"]}
}</code></pre>

    <h3>🔍 3. Obter Todos os Clientes</h3>
    <p><b>Rota:</b> <code>GET /cliente</code></p>
    <p><b>Exemplo de Resposta:</b></p>
    <pre><code>{
    "1": {"nome": "João Silva", "email": "joao@email.com", "data_cadastro": "2020-05-15", "gêneros_favoritos": ["Ficção", "Mistério"], "livros_comprados": ["1", "3"]}
}</code></pre>

    <h3>🆕 4. Adicionar um Novo Livro</h3>
    <p><b>Rota:</b> <code>POST /add_livro</code></p>
    <p><b>Formato JSON:</b></p>
    <pre><code>{
    "título": "Novo Livro", "autor_id": "2", "ano_publicacao": 2022, "gênero": "Fantasia", "preco": 50.00
}</code></pre>

    <h3>📝 5. Atualizar um Livro</h3>
    <p><b>Rota:</b> <code>PUT /up_livro</code></p>
    <p><b>Formato JSON:</b></p>
    <pre><code>{
    "id": "1", "preco": 49.90
}</code></pre>

    <h3>📝 6. Atualizar um Autor</h3>
    <p><b>Rota:</b> <code>PUT /up_livros</code></p>
    <p><b>Formato JSON:</b></p>
    <pre><code>{
    "id": "1", "nacionalidade": "Portuguesa"
}</code></pre>

    <h3>📝 7. Atualizar um Cliente</h3>
    <p><b>Rota:</b> <code>PUT /up_clientes</code></p>
    <p><b>Formato JSON:</b></p>
    <pre><code>{
    "id": "2", "email": "novo.email@mail.com"
}</code></pre>

    <h3>🗑 8. Deletar um Livro</h3>
    <p><b>Rota:</b> <code>DELETE /delete_livro/&lt;id&gt;</code></p>
    <p><b>Exemplo:</b> <code>DELETE /delete_livro/1</code></p>

    <h2>🔧 Configuração</h2>
    <p>Para rodar no modo debug e acessível na rede:</p>
    <pre><code>app.run(debug=True, host='0.0.0.0')</code></pre>

    <h2>📜 Licença</h2>
    <p>Este projeto está sob a licença MIT.</p>
</body>
</html>
