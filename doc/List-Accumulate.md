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
    custom_post_sort: 10
    field2: value 2

---
دیتای موجود در یک لیست را به صورت خلاصه شده ارائه می کند.
> _function (<code>list</code> as list, optional <code>seed</code> as nullable any, <code>accumulator</code> as function) as nullable any_

## توضیحات 
دیتای موجود در لیست  <code>list</code>  را با استفاده از تابع <code>accumulator</code> خلاصه می کند.  پارامتر, <code>seed</code> اجباری نیست و می تواند مقدار دهی نشود.
## دسته بندی 
توابع List.Transformation
## نمونه 
اعضای لیست {1, 2, 3, 4, 5} با استفاده از ((state, current) => state + current ) تجمیع می کند.
```php
List.Accumulate({1, 2, 3, 4, 5}, 0, (state, current) => state + current)
```
> 15

***
