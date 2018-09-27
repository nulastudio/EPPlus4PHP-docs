
*************
打开Excel文档
*************

.. warning:: EPPlus4PHP 仅能操作使用 Open Office Xml 格式的 Excel 2007/2010 版本文件（xlsx）

.. _open-a-normal-excel-package:

打开普通的Excel文档
===================

.. code-block:: php

    <?php

    use nulastudio\Document\EPPlus4PHP\ExcelPackage;

    $package = new ExcelPackage(__DIR__ . '/test.xlsx');

    // or
    // $package = ExcelPackage::open(__DIR__ . '/test.xlsx');

.. _open-an-encrypted-excel-package:

打开加密的Excel文档
===================

.. code-block:: php

    <?php

    use nulastudio\Document\EPPlus4PHP\ExcelPackage;

    $password = '123456';

    $package = new ExcelPackage(__DIR__ . '/test.xlsx', $password);

    // or
    // $package = ExcelPackage::open(__DIR__ . '/test.xlsx', $password);
