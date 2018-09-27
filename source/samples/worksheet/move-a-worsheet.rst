**********
移动工作表
**********

.. _move-before:

移动某工作表到指定工作表前面
============================

.. code-block:: php

    <?php

    use nulastudio\Document\EPPlus4PHP\ExcelPackage;

    $package = new ExcelPackage(__DIR__ . '/test.xlsx');

    // 将sheet1移动到sheet2前面
    $package->workBook->workSheets->moveBefore('sheet1', 'sheet2');

    // or
    // $package->workBook->workSheets['sheet1']->moveBefore('sheet2');

    $package->save();

.. _move-after:

移动某工作表到指定工作表后面
============================

.. code-block:: php

    <?php

    use nulastudio\Document\EPPlus4PHP\ExcelPackage;

    $package = new ExcelPackage(__DIR__ . '/test.xlsx');

    // 将sheet2移动到sheet1后面
    $package->workBook->workSheets->moveAfter('sheet2', 'sheet1');

    // or
    // $package->workBook->workSheets['sheet2']->moveAfter('sheet1');

    $package->save();

.. _move-to-start:

移动某工作表到最前面
====================

.. code-block:: php

    <?php

    use nulastudio\Document\EPPlus4PHP\ExcelPackage;

    $package = new ExcelPackage(__DIR__ . '/test.xlsx');

    $package->workBook->workSheets->moveToStart('sheet1');

    // or
    // $package->workBook->workSheets['sheet1']->moveToStart();

    $package->save();

.. _move-to-end:

移动某工作表到最后面
====================

.. code-block:: php

    <?php

    use nulastudio\Document\EPPlus4PHP\ExcelPackage;

    $package = new ExcelPackage(__DIR__ . '/test.xlsx');

    $package->workBook->workSheets->moveToEnd('sheet1');

    // or
    // $package->workBook->workSheets['sheet1']->moveToEnd();

    $package->save();

