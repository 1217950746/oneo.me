---
title: 'WPF 字符串格式化'
date: 2020-7-28 11:53
---

货币格式

```xml
<!-- $123.46 -->
<TextBlock Text="{Binding Price, StringFormat={}{0:C}}" />
<!-- $123.5 -->
<TextBlock Text="{Binding Price, StringFormat={}{0:C1}}" />
```

指定长度

```xml
<!-- 086723 -->
<TextBlock Text="{Binding Count, StringFormat={}{0:D6}}" />
<!-- 28768234.9329 -->
<TextBlock Text="{Binding Total, StringFormat={}{0:F4}}" />
<!-- 28,768,234.933 -->
<TextBlock Text="{Binding Total, StringFormat={}{0:N3}}" />
```

百分比

```xml
<!-- 78.9 % -->
<TextBlock Text="{Binding Persent, StringFormat={}{0:P1}}" />
```

占位符

```xml
<!-- 0123.46 -->
<TextBlock Text="{Binding Price, StringFormat={}{0:0000.00}}" />
<!-- 123.46 -->
<TextBlock Text="{Binding Price, StringFormat={}{0:####.##}}" />
```

日期

```xml
<!-- 5/4/2015 -->
<TextBlock Text="{Binding DateTimeNow, StringFormat={}{0:d}}" />
<!-- Monday, May 04, 2015 -->
<TextBlock Text="{Binding DateTimeNow, StringFormat={}{0:D}}" />
<!-- Monday, May 04, 2015 5:46 PM -->
<TextBlock Text="{Binding DateTimeNow, StringFormat={}{0:f}}" />
<!-- Monday, May 04, 2015 5:46:56 PM -->
<TextBlock Text="{Binding DateTimeNow, StringFormat={}{0:F}}" />
<!-- 5/4/2015 5:46 PM -->
<TextBlock Text="{Binding DateTimeNow, StringFormat={}{0:g}}" />
<!-- 5/4/2015 5:46:56 PM -->
<TextBlock Text="{Binding DateTimeNow, StringFormat={}{0:G}}" />
<!-- May 04 -->
<TextBlock Text="{Binding DateTimeNow, StringFormat={}{0:m}}" />
<!-- May 04 -->
<TextBlock Text="{Binding DateTimeNow, StringFormat={}{0:M}}" />
<!-- 5:46 PM -->
<TextBlock Text="{Binding DateTimeNow, StringFormat={}{0:t}}" />
<!-- 5:46:56 PM -->
<TextBlock Text="{Binding DateTimeNow, StringFormat={}{0:T}}" />
<!-- 2015年05月04日 -->
<TextBlock Text="{Binding DateTimeNow, StringFormat={}{0:yyyy年MM月dd日}}" />
<!-- 2015-05-04 -->
<TextBlock Text="{Binding DateTimeNow, StringFormat={}{0:yyyy-MM-dd}}" />
<!-- 2015-05-04 17:46 -->
<TextBlock Text="{Binding DateTimeNow, StringFormat={}{0:yyyy-MM-dd HH:mm}}" />
<!-- 2015-05-04 17:46:56 -->
<TextBlock Text="{Binding DateTimeNow, StringFormat={}{0:yyyy-MM-dd HH:mm:ss}}" />
```
