**********
合并单元格
**********

.. _merge:

合并单元格
==========

.. code-block:: php

    <?php

    use nulastudio\Document\EPPlus4PHP\ExcelPackage;

    $package = new ExcelPackage(__DIR__ . '/test.xlsx');

    $worksheet = $package->workBook->workSheets['sheet1'];

    $worksheet->cells['A1:B1'].merge = true;
    $worksheet->cells['A1:B1'].value = 'merged';
    $worksheet->cells['A1:B1'].style.horizontalAlignment = HorizontalAlignment::Center;
    $worksheet->cells['A1:B1'].style.verticalAlignment = VerticalAlignment::Center;

    $package->save();

.. _unmerge:

拆分单元格
==========

.. code-block:: php

    <?php

    use nulastudio\Document\EPPlus4PHP\ExcelPackage;

    $package = new ExcelPackage(__DIR__ . '/test.xlsx');

    $worksheet = $package->workBook->workSheets['sheet1'];

    $worksheet->cells['A1:B1'].merge = false;

    $package->save();
