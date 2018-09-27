**********
BorderItem
**********

.. _properties:

属性
----

+----------------------------------+-------+----------+
| 类型                             | 属性  | 说明     |
+==================================+=======+==========+
| :doc:`BorderStyle <BorderStyle>` | style | 边框样式 |
+----------------------------------+-------+----------+
| :doc:`Color <Color>`             | color | 边框颜色 |
+----------------------------------+-------+----------+

.. hint:: style属性可直接接受 BorderStyle 下的常量值

    - $borderItem->style = BorderStyle::DashDot;

.. hint:: color属性可直接接受 Color 下的常量值以及接受数值类型的ARGB值或者字符串类型的“#AARRGGBB”、“#RRGGBB”

    - $borderItem->color = new Color(A, R, G, B);
    - $borderItem->color = Color::GRAY_COLOR;
    - $borderItem->color = 0x00ABCDEF;
    - $borderItem->color = '#00ABCDEF';
    - $borderItem->color = '#ABCDEF';
