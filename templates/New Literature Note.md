## {{title}}

>[!md] Metadata
> **Authors**:: {{authors}}
> **Title**:: {{title}}  
> **Year**:: {{date | format("YYYY")}}   
> **Citekey**:: {{citekey}} {%- if itemType %}  
> **itemType**:: {{itemType}}{%- endif %}{%- if itemType == "journalArticle" %}  
> **Journal**:: *{{publicationTitle}}* {%- endif %}{%- if volume %}  
> **Volume**:: {{volume}} {%- endif %}{%- if issue %}  
> **Issue**:: {{issue}} {%- endif %}{%- if itemType == "bookSection" %}  
> **Book**:: {{publicationTitle}} {%- endif %}{%- if publisher %}  
> **Publisher**:: {{publisher}} {%- endif %}{%- if place %}  
> **Location**:: {{place}} {%- endif %}{%- if pages %}   
> **Pages**:: {{pages}} {%- endif %}{%- if DOI %}  
> **DOI**:: {{DOI}} {%- endif %}{%- if ISBN %}  
> **ISBN**:: {{ISBN}} {%- endif %}
> **URL**: [Original Source]({{url}})

> [!abstract]
> {{abstractNote }}

> [!cite] Cite
> {{bibliography}}

### Annotations
{% for annotation in annotations -%}
  {%- if annotation.annotatedText %}
> [!Highlight]
> {{annotation.annotatedText | replace(" ", " ") | replace("\n", "\n> ") }} 
> [Page {{annotation.page}}](zotero://open-pdf/library/items/{{annotation.attachment.itemKey}}?page={{annotation.page}}&annotation={{annotation.id}})
  {%- elif annotation.imageRelativePath %}
![[{{annotation.imageRelativePath}}]] 
  {%- elif annotation.comment %}
{{annotation.comment  | replace(" ", " ") | replace("???", ">[!question] ")  | replace("!!!", ">[!important] ") | replace("$$$", ">[!quote] ")}}
  {%- endif %}
{% endfor %}
