****
对齐
****

.. code-block:: php

    <?php

    use nulastudio\Document\EPPlus4PHP\ExcelPackage;

    $package = new ExcelPackage(__DIR__ . '/test.xlsx');

    $worksheet = $package->workBook->workSheets['sheet1'];

    $worksheet->cells['A1'].style.horizontalAlignment = HorizontalAlignment::Center;
    $worksheet->cells['A1'].style.verticalAlignment = VerticalAlignment::Center;

    $package->save();

.. hint:: 更多请查看API文档 :doc:`HorizontalAlignment </api/nulastudio/Document/EPPlus4PHP/Style/HorizontalAlignment>` 和 :doc:`VerticalAlignment </api/nulastudio/Document/EPPlus4PHP/Style/VerticalAlignment>` 部分
