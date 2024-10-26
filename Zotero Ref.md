---
status: automatically-imported
year: "{{date | format ('YYYY')}}"
authors: "{{authors}}"
type: "{{ item.itemType }}"
publisher: "{{publicationTitle}}"
collection: "{{collections[0].fullPath}}"
---
## {{title}} 
> [!info] 
> - **Sources**: [online]({{url}}) [local]({{desktopURI}}){% for attachment in attachments | filterby("path", "endswith",".pdf") %} [pdf](file:///{{attachment.path | replace(" ","%20")}}){% endfor %}
> - **DOI:** {{DOI}}
> - **Cite Key:** [[{{citekey}}]] 
{%- if hashTags %}
> - **Abstract:** {{abstractNote}}
> - **Tags:** {{hashTags}} 
{%- endif %}

>[!Personal Summary] 
> Insert personal summary here. 

> [!Authors]
> [[{{ authors | replace(', ', ']], [[') }}]]
