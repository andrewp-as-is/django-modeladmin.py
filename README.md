[![](https://img.shields.io/badge/released-2021.6.22-green.svg?longCache=True)](https://pypi.org/project/django-modeladmin/)
[![](https://img.shields.io/badge/license-Unlicense-blue.svg?longCache=True)](https://unlicense.org/)

### Installation
```bash
$ pip install django-modeladmin
```

### Pros
+   auto `list_display` (all fields)
+   auto `list_filter` (`BooleanField` fields)
+   auto `search_fields` (`CharField` and `TextField` fields)
+   `list_display` formatters - `elapsed`, `strftime`, `timesince`

### Examples
`admin.py`
```python
from django_modeladmin import admin

from .models import MyModelAdmin

@admin.register(Author)
class MyModelAdmin(admin.ModelAdmin):
    ...
```

`list_display` formatters:
```python
list_display = [
    'id',
    'started_at',
    ('strftime','started_at','%H-%M-%S','started',),
    ('elapsed','started_at','finished_at','elapsed',),
    ('timesince','created_at','',),
]
```

