**********
创建工作表
**********

.. _manually-create:

手动创建
========

.. code-block:: php

    <?php

    use nulastudio\Document\EPPlus4PHP\ExcelPackage;

    $package = new ExcelPackage(__DIR__ . '/test.xlsx');

    $package->workBook->workSheets->add('new sheet');

    $package->save();

.. _auto-create:

自动创建
========

.. code-block:: php

    <?php

    use nulastudio\Document\EPPlus4PHP\ExcelPackage;

    $package = new ExcelPackage(__DIR__ . '/test.xlsx');

    // 如果工作表不存在将会自动创建
    $worksheet = $package->workBook->workSheets['new sheet'];

    // 使用位置索引无法自动创建
    // $worksheet = $package->workBook->workSheets[8];

    $package->save();

.. warning:: 自动创建仅针对于使用表名索引，使用位置索引无法自动创建
