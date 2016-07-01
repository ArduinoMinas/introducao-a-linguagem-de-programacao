# Imagens
 
  {% for picture in book.picturesList %}
    1. [ {{ picture.list_caption }} ]( {{ picture.backlink }} )
  {% endfor %}