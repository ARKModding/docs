---
sidebar_position: 30
---

# Adding an image

You will likely want to add images to your page. 

First, place the image in the corresponding folder in the `static/img` directory. For example for this page you would place it in `static/img/docs/contrib/modify`.

:::tip
Make sure to give the image a descriptive file name!
:::

Then, add the image to your page using the following syntax:

```markdown

![Image Description](/img/docs/contrib/modify/my_test_image.png)

```

:::info
Note that the path starts with `/img/docs/` and then contains the path to the image relative to the `static/img` folder.
:::
