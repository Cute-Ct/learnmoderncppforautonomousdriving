# 必须使用模板类的情况

{% hint style="info" %}
**Good to know:** your product docs aren't just a reference of all your features! use them to encourage folks to perform certain actions and discover the value in your product.
{% endhint %}

## 如果一个类使用了stl类型，这个类也要定义为模板类

stl中的类型比如`vector` `shared_ptr`都是模板类。如果一个类`NewClass`内部使用了stl类型，`NewClass`也要设计成模板类，因为模板类型参数，只能一级一级传递进去到内部类型。

```
template <typename PointT>
struct PointCloudMsg
{
  typedef std::vector<PointT> PointCloud;
  typedef std::shared_ptr<PointCloud> PointCloudPtr;
  
  PointCloudPtr point_cloud_ptr;  ///< Point cloud pointer
  PointCloudMsg() = default;
  explicit PointCloudMsg(const PointCloudPtr& ptr) : point_cloud_ptr(ptr)
  {
  }
};
```

上面类型`PointCloudMsg`，由于内部要使用`vector`和`shared_ptr`，而这2个类型都是模板类型，需要类型参数，所以作为类型定义，`PointCloudMsg`要把模板类型参数传递进去。



那么问题来了，为什么`vector` `shared_ptr`需要模板参数呢？



