备注
====

.. _add-a-comment:

.. code-block:: php

    <?php

    use nulastudio\Document\EPPlus4PHP\ExcelPackage;

    $package = new ExcelPackage(__DIR__ . '/test.xlsx');

    $worksheet = $package->workBook->workSheets['sheet1'];

    $worksheet->cells['A1'].comment = "我是备注";

    $package->save();

.. warning:: 当已存在备注时，使用这种方式赋值将导致author被覆盖为默认的备注人！

.. _modify-a-comment:

.. code-block:: php

    <?php

    use nulastudio\Document\EPPlus4PHP\ExcelPackage;

    $package = new ExcelPackage(__DIR__ . '/test.xlsx');

    $worksheet = $package->workBook->workSheets['sheet1'];

    $worksheet->cells['A1'].comment.text = "备注2";
    $worksheet->cells['A1'].comment.author = "LieAuer";

    $package->save();

.. _delete-a-comment:

.. code-block:: php

    <?php

    use nulastudio\Document\EPPlus4PHP\ExcelPackage;

    $package = new ExcelPackage(__DIR__ . '/test.xlsx');

    $worksheet = $package->workBook->workSheets['sheet1'];

    $worksheet->cells['A1'].comment = null;

    $package->save();
