---
layout: default
---
Nakamoto Archives

# [View the Earliest Version of Bitcoin.org HERE](/bitcoinorg/20090131)

<hr>

Over the past few many years, a deliberate and well-funded effort has gone into rewriting the history of Bitcoin.



{% assign documents = site.documents | sort: 'date' | reverse %}

{% for document in documents limit:500 %}
  {% if document.layout == 'email' %}
<div class="article">
        <span class="date">{{ document.date | date: "%Y-%m-%d" }}</span>

             {% if document.layout == "post" %} <span class="title">   <a href="{{ document.url | relative_url }}">{{ document.title }} </a>
         </span>{% elsif document.layout == "link" %} <span class="title">   <a href="{{ document.link | relative_url }}"> {{ document.title }} | {{ document.site }} </a>→
         </span> 
         
        {% else %} <span class="title">   <a href="{{ document.url | relative_url }}">{{ document.date | date: "%H:%M:%S" }}   </a>
         </span>  {% endif %}
       
       
     
      
         
        
 </div> 
  {% endif %}   
{% endfor %}
