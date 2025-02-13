{%- set unique_domains = states | map(attribute='domain') | list | unique | list -%}
{%- for domain in unique_domains -%}
{{domain + "\n"}}
{%- endfor -%}

entities:

{%- for state in states -%}
{{state.entity_id + "\n"}}
{%- endfor -%}
