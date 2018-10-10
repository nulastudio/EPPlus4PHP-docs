****
公式
****

.. hint:: 书写支持大小写风格，建议大写风格

.. hint:: 不支持地区命名，如“求和”

.. _using-built-in-formula:

使用内置公式
============

.. code-block:: php

    <?php

    use nulastudio\Document\EPPlus4PHP\ExcelPackage;

    $package = new ExcelPackage(__DIR__ . '/test.xlsx');

    $worksheet = $package->workBook->workSheets['sheet1'];

    $worksheet->cells['A2'].value = 2;
    $worksheet->cells['A3'].value = 3;

    $worksheet->cells['A1'].formula = 'SUM(A2,A3)';

    // 5
    var_dump($worksheet->cells['A1'].value);

    $package->save();

.. hint:: `支持的内置函数列表 <https://github.com/nulastudio/EPPlus4PHP/blob/master/EPPlus4PHP.Core/supported-builtin-functions.md>`_

.. _using-built-in-formula-R1C1:

使用R1C1样式的公式
==================

.. code-block:: php

    <?php

    use nulastudio\Document\EPPlus4PHP\ExcelPackage;

    $package = new ExcelPackage(__DIR__ . '/test.xlsx');

    $worksheet = $package->workBook->workSheets['sheet1'];

    $worksheet->cells['A2'].value = 2;
    $worksheet->cells['A3'].value = 3;

    $worksheet->cells['A1'].formulaR1C1 = 'SUM(R2C1,R3C1)';

    // 5
    var_dump($worksheet->cells['A1'].value);

    $package->save();

.. _using-user-defined-formula:

使用自定义公式
==============

.. code-block:: php

    <?php

    use nulastudio\Document\EPPlus4PHP\ExcelPackage;

    $package = new ExcelPackage(__DIR__ . '/test.xlsx');

    $worksheet = $package->workBook->workSheets['sheet1'];

    $worksheet->cells['A2'].value = 2;
    $worksheet->cells['A3'].value = 3;

    // 添加一个自定义函数
    $package->addOrReplaceFunction('MYSUM', function(array $args, array $context) {
        list($a, $b) = $args;
        return $a + $b;
    });

    $worksheet->cells['A1'].formula = 'MYSUM(A2,A3)';

    // 5
    // 注意：只能在程序中取值，Excel中无法取值，因为Excel并不存在mysum函数
    var_dump($worksheet->cells['A1'].value);

    $package->save();

.. hint:: 自定义公式接受两个参数且返回一个结果值。

    - array $args 传入的参数数组
    - array $context 当前的上下文数组（目前尚未决定需要哪些上下文，暂时为空）


.. hint:: 在有能力编写复杂内置公式和VBA的情况下尽量少用自定义公式，因为涉及到自定义公式的单元格只能在EPPlus4PHP中取值，Excel中是无法取值的！

.. hint:: 在未来版本会增加计算公式表达式并取值以及VBA的功能，可计算后存值或者编写VBA，Excel就能获取到值。

.. hint:: 由于自定义公式只能在程序中取值，所以自定义公式可以接受及返回任意类型的参数，只不过当与内置函数混用时确保传入到内置函数时Excel支持的基本类型即可。
