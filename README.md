# Tocoista-Criar uma rede social simples requer um pouco mais de complexidade, mas aqui está um modelo básico usando HTML, CSS e JavaScript. Este exemplo inclui uma estrutura inicial para um site de rede social.

### Estrutura Básica de uma Rede Social

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rede Social Tocoistas</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        header {
            background: #333;
            color: #fff;
            padding: 10px 20px;
            text-align: center;
        }
        .container {
            max-width: 800px;
            margin: 20px auto;
            padding: 20px;
            background: #fff;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        .post {
            border: 1px solid #ddd;
            border-radius: 5px;
            margin: 10px 0;
            padding: 15px;
        }
        .post h3 {
            margin: 0;
        }
        .form-post {
            margin: 20px 0;
        }
        .form-post textarea {
            width: 100%;
            height: 60px;
        }
        .form-post button {
            margin-top: 10px;
            padding: 10px;
            background: #333;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
    </style>
</head>
<body>

<header>
    <h1>Rede Social Tocoistas</h1>
</header>

<div class="container">
    <div class="form-post">
        <h2>Crie um novo post</h2>
        <textarea id="postContent" placeholder="O que você está pensando?"></textarea>
        <button onclick="addPost()">Publicar</button>
    </div>
    
    <div id="posts">
        <h2>Posts Recentes</h2>
        <!-- Posts serão adicionados aqui -->
    </div>
</div>

<script>
    function addPost() {
        const content = document.getElementById('postContent').value;
        if (content) {
            const postContainer = document.getElementById('posts');
            const postElement = document.createElement('div');
            postElement.className = 'post';
            postElement.innerHTML = `<h3>Tocoista</h3><p>${content}</p>`;
            postContainer.prepend(postElement);
            document.getElementById('postContent').value = '';
        } else {
            alert('Por favor, escreva algo!');
        }
    }
</script>

</body>
</html>
```

### Descrição do Modelo

- **Header**: Título da rede social.
- **Formulário de Postagem**: Área para os usuários criarem novos posts.
- **Lista de Posts**: Onde os posts dos usuários serão exibidos.
- **JavaScript**: Para adicionar novos posts dinamicamente.

### Personalizações

1. **Estilo**: Você pode modificar o CSS para adequar ao visual desejado.
2. **Funcionalidade**: Este é um exemplo muito básico. Para funcionalidades como login, comentários, ou interações, você precisaria de um backend (por exemplo, usando Node.js, PHP, ou uma plataforma como Firebase).

### Próximos Passos

- **Backend**: Para armazenar posts e usuários, você precisaria de um banco de dados e um servidor.
- **Autenticação**: Adicionar um sistema de login para usuários.
- **Interatividade**: Implementar comentários, curtidas e outras interações.

Se precisar de mais informações ou ajuda em um aspecto específico, é só avisar!
