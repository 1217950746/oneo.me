---
title: 'WPF 多重绑定'
date: 2020-7-28 11:53
---

## 多重绑定

```xml
<TextBox.Text>
    <MultiBinding StringFormat="姓名：{0}{1}">
        <Binding Path="FristName" />
        <Binding Path="LastName" />
    </MultiBinding>
</TextBox.Text>
```
