Readme
======


Installation
------------



Licensing
---------

All code unless otherwise noted is licensed under the terms of the MIT License (MIT). Please refer to the file LICENSE in the root directory of this repository.


Install the package
------------

`pip install acdh-django-sparql`

# mandatory:

## add `sparql` to `INSTALLED_APPS`

```
...
'apis_core.apis_entities',
'apis_core.apis_metainfo',
'apis_core.apis_relations',
'apis_core.apis_vocabularies',
'apis_core.apis_labels',
...
```

## add apis specific context_processors

```
'OPTIONS': {
    'context_processors': [
        ...
        'webpage.webpage_content_processors.is_dev_version',
        'apis_core.context_processors.custom_context_processors.add_entities',
        ...
    ],
},
```
