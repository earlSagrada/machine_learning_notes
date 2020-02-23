```python
ds_tensors = tf.data.Dataset.from_tensor_slices([1, 2, 3, 4, 5, 6])

# Create a CSV file
import tempfile
_, filename = tempfile.mkstemp()

with open(filename, 'w') as f:
  f.write("""Line 1
Line 2
Line 3
  """)

ds_file = tf.data.TextLineDataset(filename)
```
```mkstemp()```返回一个元组，元组中第一个元素是句柄，它是一个系统级句柄，指向一个打开的文件（等同于```os.open()```的返回值），第二元素是该文件的绝对路径。

```_```
用作被丢弃的名称。按照惯例，这样做可以让阅读你代码的人知道，这是个不会被使用的特定名称。
可以返回上一次的运行结果

ref:
https://juejin.im/post/5bf16f33e51d4512d23d08b4
https://www.cnblogs.com/alan-babyblog/p/5227920.html
