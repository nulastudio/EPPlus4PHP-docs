****
填充
****

.. code-block:: php

    <?php

    use nulastudio\Document\EPPlus4PHP\ExcelPackage;

    $package = new ExcelPackage(__DIR__ . '/test.xlsx');

    $worksheet = $package->workBook->workSheets['sheet1'];

    $worksheet->cells['A1'].style.fill.backgroundColor = Color::YELLOW_COLOR;

    $package->save();

.. hint:: 更多请查看API文档 :doc:`Fill </api/nulastudio/Document/EPPlus4PHP/Style/Fill>` 部分
