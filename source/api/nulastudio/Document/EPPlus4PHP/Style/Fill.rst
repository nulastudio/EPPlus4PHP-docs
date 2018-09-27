****
Fill
****

.. _properties:

属性
----

+----------------------+-----------------+----------+
| 类型                 | 属性            | 说明     |
+======================+=================+==========+
| :doc:`Color <Color>` | backgroundColor | 填充颜色 |
+----------------------+-----------------+----------+

.. hint:: backgroundColor属性可直接接受 Color 下的常量值以及接受数值类型的ARGB值或者字符串类型的“#AARRGGBB”、“#RRGGBB”

    - $fill->backgroundColor = new Color(A, R, G, B);
    - $fill->backgroundColor = Color::GRAY_COLOR;
    - $fill->backgroundColor = 0x00ABCDEF;
    - $fill->backgroundColor = '#00ABCDEF';
    - $fill->backgroundColor = '#ABCDEF';
