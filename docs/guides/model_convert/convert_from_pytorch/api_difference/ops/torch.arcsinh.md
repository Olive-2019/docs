## [torch 参数更多 ]torch.arcsinh

### [torch.arcsinh](https://pytorch.org/docs/stable/generated/torch.arcsinh.html#torch.arcsinh)

```python
torch.arcsinh(input,
             *,
             out=None)
```

### [paddle.asinh](https://www.paddlepaddle.org.cn/documentation/docs/zh/develop/api/paddle/asinh_cn.html)

```python
paddle.asinh(x,
            name=None)
```

Pytorch 相比 Paddle 支持更多其他参数，具体如下：

### 参数映射
| PyTorch       | PaddlePaddle | 备注                                                   |
| ------------- | ------------ | ------------------------------------------------------ |
| input         | x            | 输入的 Tensor ，仅参数名不一致。                                      |
| out           | -            | 表示输出的 Tensor ，Paddle 无此参数，需要转写。               |


### 转写示例
#### out：指定输出
```python
# Pytorch 写法
torch.arcsinh(torch.tensor([-0.5962,  0.4985]), out=y)

# Paddle 写法
paddle.assign(paddle.asinh(paddle.to_tensor([-0.5962,  0.4985])), y)
```
