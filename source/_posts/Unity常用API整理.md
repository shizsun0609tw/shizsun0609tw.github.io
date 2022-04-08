---
title: Unity常用API整理
date: 2022-04-07 15:44:46
tags:
- Unity
category:
- Unity
---

* [Vector](#Vector)
* [Quaternion](#Quaternion)
* [Mathf](#Mathf)
* [Random](#Random)

<!--more-->

---

## Vector

[doc](https://docs.unity3d.com/ScriptReference/Vector3.html)

### Constructor

```cs
Vector3 vector = new Vector3(0f, 0f, 0f);
```

### 長度

```cs
float length = vectorA.magnitude;
```

### Normalized

```cs
Vector3 v = vectorA.normalized;
```

### 距離

```cs
float distance = Vector3.Distance(Vector3 vectorA, Vector3 vectorB);
```

### 向量間夾角

```cs
float angle = Vector3.Angle(Vector3 vectorFrom, Vector3 vectorTo);
```

### 內積

```cs
float res = Vector3.Dot(Vector3 vectorA, Vector3 vectorB);
```

### 外積

```cs
Vector3 res = Vector3.Cross(Vector3 vectorA, Vector3 vectorB).normalized;
```
---

## Quaternion

[doc](https://docs.unity3d.com/ScriptReference/Quaternion.html)

### Constructor

```cs
Quaternion q = new Quaternion();
Quaternion q = Quaternion.identity;
Quaternion q = Quaternion.Euler(0, 0, 0);
```

### EulerAngle

```cs
Vector3 rotations = quaternion.eulerAngles;
```

### 兩向量間的旋轉

```cs
quaternion.SetFromToRotation(Vector3 vectorFrom, Vector3 vectorTo);
```

### 看向某向量

```cs
quaternion.SetLookRotation(Vector3 vectorView, Vector3 vectorUp=Vector3.up);
```

### 旋轉向量

```cs
Vector3 direction = Quaternion.Euler(0, 90, 0) * vectorA;
```

---

## Mathf

### Constant

```cs
float pi = Mathf.PI;
float epsilon = Mathf.Epsilon;
float rad = deg * Mathf.Deg2Rad;
float inf = Mathf.Infinity;
```

### Clamp

```cs
float clamp = Mathf.Clamp(float value, float min, float max);
```

### Abs

```cs
float abs = Mathf.Abs(float value);
```

### Min, Max

```cs
float max = Mathf.Max(float valueA, float valueB);
float min = Mathf.Min(float valueA, float valueB);
```

### Sign

```cs
float sign = Mathf.Sign(float value);
```

---

## Random

[doc](https://docs.unity3d.com/ScriptReference/Random.html)

### Random

```cs
float rnd = Random.Range(float min, float max);
```