# Singleton（单例）

## Getting Super Powers

这里我们使用泛型来定义所有类，这样可以满足不同类的单例继承。

{% code title="Singleton.cs" %}
```bash
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Singleton<T> : MonoBehaviour 
    where T : new()
{
    private static T instance;
    public static T Instance
    {
        get
        {
            if (instance == null)
            {
                instance = new T();
            }
            return instance;
        }
    }
    
    protected Singleton(){ }
}
```
{% endcode %}



