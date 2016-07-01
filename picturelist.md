# Imagens
 
  {% for picture in book.picturesList %}
    1. [{{ page.picture.list_caption }}]({{ page.picture.backlink }})
  {% endfor %}