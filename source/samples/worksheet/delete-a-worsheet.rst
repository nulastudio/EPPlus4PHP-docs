**********
删除工作表
**********

.. code-block:: php

    <?php

    use nulastudio\Document\EPPlus4PHP\ExcelPackage;

    $package = new ExcelPackage(__DIR__ . '/test.xlsx');

    $package->workBook->workSheets->delete('sheet1');

    $package->save();
