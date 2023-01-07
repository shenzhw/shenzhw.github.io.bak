---
title: "如何优雅使用Optional"
date: 2023-01-07T23:35:58+08:00
draft: false
---

# 如何优雅使用Optional

- 代码片段1
```Java
public static String getName(User user) {
    if (user == null) {
        return "unknown";
    }
    return user.getName();
}
```
改为：
```Java
public static String getName(User user) {
    return Optional.ofNullable(user).map(u -> u.getName()).orElse("unknown");
}
```

- 代码片段2
```Java
public static String getChampionName(Competition comp) throws IllegalArgumentException {
    if (comp != null) {
        CompResult result = comp.getResult();
        if (result != null) {
            User champion = result.getChampion();
            if (champion != null) {
                return champion.getName();
            }
        }
    }
    throw new IllegalArgumentException("The value of param comp isn't available.");
}
```
改为
```Java
public static String getChampionName(Competition comp) throws IllegalArgumentException {
    return Optional.ofNullable(comp).map(Competition::getResult).map(CompResult::getChampion).map(User::getName).orElseThrow(() ->new IllegalArgumentException("The value of param comp isn't available."));
}
```

- 字符串为空则不打印
```java
public static void print(String name) {
    Optional.ofNullable(name).ifPresent(System.out::println);
}
```
