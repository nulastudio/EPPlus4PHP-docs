************
ExcelConvert
************

.. _methods:

方法
----

+--------+----------------------------------------------------+-----------------------------------------------------------+
| 返回值 | 方法签名                                           | 说明                                                      |
+========+====================================================+===========================================================+
| int    | public static function toIndex(string $columnName) | 将二十六进制的单元格格式转换成十进制的单元格格式，从1开始 |
+--------+----------------------------------------------------+-----------------------------------------------------------+
| string | public static function toName(int $index)          | 将十进制的单元格格式转换成二十六进制的单元格格式，从1开始 |
+--------+----------------------------------------------------+-----------------------------------------------------------+

.. _examples:

示例
----

.. code-block:: php

    <?php

    use nulastudio\Document\EPPlus4PHP\ExcelConvert;

    $column_index1 = ExcelConvert::toIndex('XFD');
    $column_name1 = ExcelConvert::toName(16384);

    $column_index2 = ExcelConvert::toIndex('A');
    $column_name2 = ExcelConvert::toName(1);

    vard_dump($column_index1, $column_name1, $column_index2, $column_name2);

    // 输出 16384, XFD, 1, A
