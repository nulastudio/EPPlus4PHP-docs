**********
选择工作表
**********

.. _string-index:

使用表名选择工作表
==================

.. code-block:: php

    <?php

    use nulastudio\Document\EPPlus4PHP\ExcelPackage;

    $package = new ExcelPackage(__DIR__ . '/test.xlsx');

    $worksheet = $package->workBook->workSheets['sheet1'];

    // do something

    $package->save();

.. _number-index:

使用位置选择工作表
==================

.. code-block:: php

    <?php

    use nulastudio\Document\EPPlus4PHP\ExcelPackage;

    $package = new ExcelPackage(__DIR__ . '/test.xlsx');

    $worksheet = $package->workBook->workSheets[1];

    // do something

    $package->save();

.. warning:: 索引从1开始
