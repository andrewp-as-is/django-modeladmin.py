[![](https://img.shields.io/badge/released-2021.6.22-green.svg?longCache=True)](https://pypi.org/project/django-modeladmin/)
[![](https://img.shields.io/badge/license-Unlicense-blue.svg?longCache=True)](https://unlicense.org/)

### Installation
```bash
$ pip install django-modeladmin
```

### Pros
+   auto `list_display` (all fields)
+   auto `search_fields` (`CharField` and `TextField` fields)
+   auto `list_filter` (`BooleanField` fields)

### Examples
```python
from django_modeladmin import admin

from .models import MyModelAdmin

@admin.register(Author)
class MyModelAdmin(admin.ModelAdmin):
    ...
```

