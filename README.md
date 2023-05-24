<!DOCTYPE html>
<html>
<head>
  <title>Mi tu puta madre</title>
</head>
<body>
  <h1>Mi Página Web</h1>
  <p>Bienvenido a mi página web. Aquí puedes agregar tus comentarios.</p>

  <form id="comment-form">
    <label for="name">Nombre:</label>
    <input type="text" id="name" name="name"><br>

    <label for="comment">Comentario:</label><br>
    <textarea id="comment" name="comment" rows="4" cols="50"></textarea><br>

    <input type="submit" value="Enviar comentario">
  </form>

  <div id="comments">
    <!-- Los comentarios se mostrarán aquí -->
  </div>

  <script>
    // Obtener el formulario de comentarios
    const commentForm = document.getElementById('comment-form');

    // Agregar un evento de envío al formulario
    commentForm.addEventListener('submit', function(event) {
      event.preventDefault(); // Evitar el envío del formulario

      // Obtener los valores del formulario
      const name = document.getElementById('name').value;
      const comment = document.getElementById('comment').value;

      // Crear un elemento de comentario
      const commentElement = document.createElement('div');
      commentElement.innerHTML = '<strong>' + name + ':</strong> ' + comment;

      // Agregar el comentario al contenedor de comentarios
      const commentsContainer = document.getElementById('comments');
      commentsContainer.appendChild(commentElement);

      // Limpiar el formulario
      commentForm.reset();
    });
  </script>
</body>
</html>
