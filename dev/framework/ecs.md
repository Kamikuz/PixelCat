# ECS

## 安装&配置

## 初始化

这里我们分为两个部分，第一个是System的初始化。

{% tabs %}
{% tab title="System 部分" %}
```csharp
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using Unity.Entities; //务必引用Eneities命名空间

public class MoveSystem : MonoBehaviour
{
    public EntityManager entityManager = World.DefaultGameObjectInjectionWorld.EntityManager;
    //新版本采用 DefaultGameObjectInjectionWorld 而非 Active 方法
}
```
{% endtab %}

{% tab title="Component 部分" %}
```csharp
using System;
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using Unity.Entities; //务必引用Eneities命名空间

public struct Demo: IComponentData //这里将继承 IComponentData 类而非 Monobehavior,同时使用结构体
{
    public int ;
}

```
{% endtab %}
{% endtabs %}



