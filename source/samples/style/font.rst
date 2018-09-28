****
字体
****

.. code-block:: php

    <?php

    use nulastudio\Document\EPPlus4PHP\ExcelPackage;

    $package = new ExcelPackage(__DIR__ . '/test.xlsx');

    $worksheet = $package->workBook->workSheets['sheet1'];

    $worksheet->cells['A1'].style.font.size = 18;
    $worksheet->cells['A1'].style.font.color = Color::RED_COLOR;
    $worksheet->cells['A1'].style.font.bold = true;

    $package->save();

.. hint:: 更多请查看API文档 :doc:`Font </api/nulastudio/Document/EPPlus4PHP/Style/Font>` 部分
