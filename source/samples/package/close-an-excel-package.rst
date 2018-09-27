*************
保存Excel文档
*************

.. warning:: 文档仅能保存一次，因为保存完会自动关闭文档，所以请确保在做完所有操作后再保存关闭文档

.. _save-an-excel-package:

保存并关闭Excel文档
===================

.. code-block:: php

    <?php

    use nulastudio\Document\EPPlus4PHP\ExcelPackage;

    $package = new ExcelPackage(__DIR__ . '/test.xlsx');

    // do something

    $package->save();

.. _save-an-excel-package-using-password:

使用密码或新密码保存并关闭Excel文档
===================================

.. code-block:: php

    <?php

    use nulastudio\Document\EPPlus4PHP\ExcelPackage;

    $password = '123456';

    $package = new ExcelPackage(__DIR__ . '/test.xlsx');

    // do something

    $package->save($password);

.. _save-an-excel-package-without-password:

取消密码保存并关闭Excel文档
===========================

.. code-block:: php

    <?php

    use nulastudio\Document\EPPlus4PHP\ExcelPackage;

    $password = '123456';

    $package = new ExcelPackage(__DIR__ . '/test.xlsx', $password);

    // do something

    $package->save(null);

.. _saveas-an-excel-package:

另存为并关闭Excel文档
=====================

.. code-block:: php

    <?php

    use nulastudio\Document\EPPlus4PHP\ExcelPackage;

    $package = new ExcelPackage(__DIR__ . '/test.xlsx');

    // do something

    $package->saveAs(__DIR__ . '/test2.xlsx');

.. _saveas-an-excel-package-using-password:

使用密码或新密码另存为并关闭Excel文档
=====================================

.. code-block:: php

    <?php

    use nulastudio\Document\EPPlus4PHP\ExcelPackage;

    $password = '123456';

    $package = new ExcelPackage(__DIR__ . '/test.xlsx');

    // do something

    $package->saveAs(__DIR__ . '/test2.xlsx', $password);

.. _saveas-an-excel-package-without-password:

取消密码另存为并关闭Excel文档
=============================

.. code-block:: php

    <?php

    use nulastudio\Document\EPPlus4PHP\ExcelPackage;

    $password = '123456';

    $package = new ExcelPackage(__DIR__ . '/test.xlsx', $password);

    // do something

    $package->saveAs(__DIR__ . '/test2.xlsx', null);
