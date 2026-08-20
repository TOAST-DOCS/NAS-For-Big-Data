{%- if "ppp" in build_flags and "ngsc" in build_flags -%}
  {%- set min_size = "1테라바이트(TB)" -%}
  {%- set max_size = "1페타바이트(PB)" -%}
  {%- set max_size_text = "1페타바이트" -%}
  {%- set network_acl_guide_url = "/Network/Network%20ACL/ko/overview-ngsc" -%}
  {%- set support_url = "https://www.ngsc.go.kr/kr/support/inquiry" -%}
  {%- set overview_capacity_prefix = "최대 1페타바이트까지 " -%}
  {%- set scale_description = "수백 테라바이트(TB) 이상의" -%}
{%- else -%}
  {#- public (기본값) -#}
  {%- set min_size = "1,000GB" -%}
  {%- set max_size = "50,000GB" -%}
  {%- set max_size_text = "" -%}
  {%- set network_acl_guide_url = "/Network/Network%20ACL/ko/overview" -%}
  {%- set support_url = "https://www.nhncloud.com/kr/support/inquiry" -%}
  {%- set overview_capacity_prefix = "" -%}
  {%- set scale_description = "" -%}
{%- endif -%}
