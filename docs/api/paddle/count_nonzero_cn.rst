.. _cn_api_paddle_count_nonzero:

count_nonzero
-------------------------------

.. py:function:: paddle.count_nonzero(x, axis=None, keepdim=False, name=None)

沿给定的轴 ``axis`` 统计输入 Tensor ``x`` 中非零元素的个数。

参数
::::::::::
   - **x** (Tensor) - 输入的 Tensor，数据类型为：bool、float16、float32、float64、int32、int64。
   - **axis** (None|int|list|tuple，可选) - 指定对 ``x`` 进行计算的轴。``axis`` 可以是 int 或者 int 元素的列表。``axis`` 值应该在范围[-D， D)内，D 是 ``x`` 的维度。如果 ``axis`` 或者其中的元素值小于 0，则等价于 :math:`axis + D`。如果 ``axis`` 是 None，则对 ``x`` 的全部元素计算中位数。默认值为 None。
   - **keepdim** (bool，可选) - 是否在输出 Tensor 中保留减小的维度。如果 ``keepdim`` 为 True，则输出 Tensor 和 ``x`` 具有相同的维度(减少的维度除外，减少的维度的大小为 1)。否则，输出 Tensor 的形状会在 ``axis`` 上进行 squeeze 操作。默认值为 True。
   - **name** (str，可选) - 具体用法请参见 :ref:`api_guide_Name`，一般无需设置，默认值为 None。


返回
::::::::::
    ``Tensor``，沿着 ``axis`` 统计输入 Tensor 中非零元素的个数，数据类型 int64。

代码示例
::::::::::

COPY-FROM: paddle.count_nonzero
