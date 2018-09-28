****
边框
****

.. code-block:: php

    <?php

    use nulastudio\Document\EPPlus4PHP\ExcelPackage;

    $package = new ExcelPackage(__DIR__ . '/test.xlsx');

    $worksheet = $package->workBook->workSheets['sheet1'];

    $worksheet->cells['A1'].style.border.top.style = BorderStyle::Dashed;
    $worksheet->cells['A1'].style.border.top.color = Color::YELLOW_COLOR;

    $worksheet->cells['A1'].style.border.bottom.style = BorderStyle::Dashed;
    $worksheet->cells['A1'].style.border.bottom.color = Color::YELLOW_COLOR;

    $worksheet->cells['A1'].style.border.left.style = BorderStyle::Dashed;
    $worksheet->cells['A1'].style.border.left.color = Color::YELLOW_COLOR;

    $worksheet->cells['A1'].style.border.right.style = BorderStyle::Dashed;
    $worksheet->cells['A1'].style.border.right.color = Color::YELLOW_COLOR;

    $package->save();

.. hint:: 更多请查看API文档 :doc:`Border </api/nulastudio/Document/EPPlus4PHP/Style/Border>` 部分
