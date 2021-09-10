# querystring-in-liquid

            {%- if canonical_url != blank  -%}
              <link rel="canonical" href="{{ canonical_url }}{%- render 'querystring-in-liquid' -%}">
            {%- endif -%}
            
            {%- capture showprogress -%}{%- render 'querystring-in-liquid' -%}{%- endcapture -%}
            {% if showprogress contains '?showprogress' %}
            <script type="text/javascript">
              $(document).ready(function(){
                $('.product-main-section').hide();
                $('.product-progress-form').show();
              });
            </script>
            {% endif %}
            
