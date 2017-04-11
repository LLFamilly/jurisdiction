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
