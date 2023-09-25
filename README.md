## Deploy
[![Deploy on Railway](https://railway.app/button.svg)](https://railway.app/template/AWUIv6)

---
title: Django Volume Support
description: A Django Template with Volume Support for Railway
tags:
  - django
  - hypercorn
  - python
---

# Django with Volume Support Example

This example template starts a Django server utilizing volume support on Railway for storing and serving assets.

## ✨ Features

- Django
- Railway Volumes
- Python 3

## 💁‍♀️ How to use

- Clone locally and install packages with pip using `pip install -r requirements.txt`
- Run locally using `hypercorn main:app --reload`

## 📝 Troubleshooting
If you get the following error `No such file or directory: '/app/media/directory/...'` make sure your directory exists since your folder structure has to be build from scratch for production purpose on the persistent storage.

You can use something like this:

```python
new_directory = os.path.join(settings.MEDIA_ROOT, 'directory')
if not os.path.exists(new_directory):
  os.makedirs(new_directory)
```
