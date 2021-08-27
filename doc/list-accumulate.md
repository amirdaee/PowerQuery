---
title: list.Accumulate
menu_order: 1
post_status: publish
post_excerpt: This is a post excerpt
taxonomy:
  category:
    - category-slug-1
    - category-slug-2
  post_tag:
    - tag-1
    - tag-2
custom_fields:
  _custom_post_order: 10
  field2: value 2
---

# List-Accumulate

دیتای موجود در یک لیست را به صورت خلاصه شده ارائه می کند.

> _function \(`list` as list, optional `seed` as nullable any, `accumulator` as function\) as nullable any_

## توضیحات

دیتای موجود در لیست `list` را با استفاده از تابع `accumulator` خلاصه می کند. پارامتر, `seed` اجباری نیست و می تواند مقدار دهی نشود.

## دسته بندی

توابع List.Transformation

## نمونه

اعضای لیست {1, 2, 3, 4, 5} با استفاده از \(\(state, current\) =&gt; state + current \) تجمیع می کند.

```php
List.Accumulate({1, 2, 3, 4, 5}, 0, (state, current) => state + current)
```

> 15

