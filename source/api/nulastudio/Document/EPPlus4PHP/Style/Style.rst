*****
Style
*****

.. _properties:

属性
----

+--------------------------------------------------+---------------------+----------------+
| 类型                                             | 属性                | 说明           |
+==================================================+=====================+================+
| :doc:`Font <Font>`                               | font                | 只读，字体     |
+--------------------------------------------------+---------------------+----------------+
| :doc:`Fill <Fill>`                               | fill                | 只读，填充     |
+--------------------------------------------------+---------------------+----------------+
| :doc:`Border <Border>`                           | border              | 只读，边框     |
+--------------------------------------------------+---------------------+----------------+
| :doc:`NumberFormat <NumberFormat>`               | numberFormat        | 只读，数字格式 |
+--------------------------------------------------+---------------------+----------------+
| :doc:`HorizontalAlignment <HorizontalAlignment>` | horizontalAlignment | 水平对齐       |
+--------------------------------------------------+---------------------+----------------+
| :doc:`VerticalAlignment <VerticalAlignment>`     | verticalAlignment   | 垂直对齐       |
+--------------------------------------------------+---------------------+----------------+

.. hint:: horizontalAlignment属性可直接接受 HorizontalAlignment 下的常量值

    - $style->horizontalAlignment = HorizontalAlignment::Center;

.. hint:: verticalAlignment属性可直接接受 VerticalAlignment 下的常量值

    - $style->verticalAlignment = VerticalAlignment::Center;
