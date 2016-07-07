# Imagens

{% for picture in book.picturesList %}
 1. [{{ picture.list_caption }}]({{ picture.backlink }})
{% endfor %}
---
[Informações sobre licença de uso das imagens podem ser obtidas clianco aqui](licenca.md).

---
Revisado: 07/07/2016 - 11:55 | Atualizado: 07/07/2016 - 11:55 | Compilado: {{ gitbook.time }}