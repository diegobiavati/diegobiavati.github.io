<!-- For styles with static names... -->
<link href="{{ 'assets/css/style.css' | relative_url }}" rel="stylesheet">
<!-- For documents/pages whose URLs can change... -->
[{{ page.title }}]("{{ page.url | relative_url }}")
