************
WorkSheets
************

.. _implements:

实现
----

`\\Iterator <http://php.net/manual/zh/class.iterator.php>`_, `\\ArrayAccess <http://php.net/manual/zh/class.arrayaccess.php>`_, `\\Countable <http://php.net/manual/zh/class.countable.php>`_

.. _properties:

属性
----

+------+---------+------+
| 类型 | 属性    | 说明 |
+======+=========+======+
| bool | is1Base | 只读 |
+------+---------+------+

.. _methods:

方法
----

+--------+--------------------------------------------------------------------+-----------------------------------------------------------+
| 返回值 | 方法签名                                                           | 说明                                                      |
+========+====================================================================+===========================================================+
| void   | public function add(string $sheetName)                             | 添加一个工作表                                            |
+--------+--------------------------------------------------------------------+-----------------------------------------------------------+
| void   | public function delete(string $sheetName)                          | 删除指定工作表                                            |
+--------+--------------------------------------------------------------------+-----------------------------------------------------------+
| void   | public function moveBefore(string $sourceName, string $targetName) | 移动工作表到指定工作表前面                                |
+--------+--------------------------------------------------------------------+-----------------------------------------------------------+
| void   | public function moveAfter(string $sourceName, string $targetName)  | 移动工作表到指定工作表后面                                |
+--------+--------------------------------------------------------------------+-----------------------------------------------------------+
| void   | public function moveToStart(string $sourceName)                    | 移动工作表到最前面                                        |
+--------+--------------------------------------------------------------------+-----------------------------------------------------------+
| void   | public function moveToEnd(string $sourceName)                      | 移动工作表到最后面                                        |
+--------+--------------------------------------------------------------------+-----------------------------------------------------------+

.. _examples:

示例
----

.. code-block:: php

    <?php

    use nulastudio\Document\EPPlus4PHP\ExcelPackage;

    $package = new ExcelPackage(__DIR__ . '/test.xlsx');
    $worksheets = $package->workBook->workSheets;

    // 统计工作表数量
    var_dump(count($worksheets));

    // 获取工作表

    // 获取第一个工作表
    $first_worksheet = $worksheets[1];
    // 获取指定工作表（不存在则创建）
    $worksheet = $worksheets['second'];

    // 遍历工作表
    foreach ($workSheets as $name => $ws) {
        // $name -> 工作表名字
        // $ws   -> 工作表对象
        var_dump($name, $ws);
    }
