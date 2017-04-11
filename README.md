# js设置属性权限
## 给属性添加权限的必要性
- 比如 文件系统 我们可以设置只允许访问,不可以修改

- 如何设置某个属性可读

- 如何设置??

## defineProperty设置权限
- Object.defineProperty(a,b,c);
- 例如：Object.defineProperty(this,"num",{
  value:200,
  writable:false,
});
- this指向当前对象，num是当前对象的属性需要加引号，设置的值固定为200
- writable 判断是否能修改，默认为ture，false则无法修改
### 关于c参数：
- 是一个用于描述属性值得json数据.
- 这个json数占领configurable，eumerable，writable，value构成
- configurable:1.可否被删除，2.他的属性值可否被批改.3.可否把属性设置成接见器属性，默认是true，可以删除，，批改，设置
- eumerable:可否被for-in轮回到
- writable:默示属性值可否被批改
- value:属性值.
## 兼容性
- 因为Object.defineProperty方法是ES5的一部分，所以在IE9及现代浏览器，IE8中只得到了部分实现。但是，如果你不需要处理旧的浏览器，defineProperty可能会有你使用的地方。
