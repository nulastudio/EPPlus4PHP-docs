**********
迭代工作表
**********

.. _count-worksheets:

获取工作表数量
==============

.. code-block:: php

    <?php

    use nulastudio\Document\EPPlus4PHP\ExcelPackage;

    $package = new ExcelPackage(__DIR__ . '/test.xlsx');

    $count = count($package->workBook->workSheets);

    var_dump("this excel package has {$count} worksheets");

.. _iterate-worksheets:

遍历工作表
==========

.. code-block:: php

    <?php

    use nulastudio\Document\EPPlus4PHP\ExcelPackage;

    $package = new ExcelPackage(__DIR__ . '/test.xlsx');

    foreach ($package->workBook->workSheets as $name => $worksheet) {
        var_dump($name, $worksheet);
    }
