---
title: protected 关键字（C# 参考）
ms.date: 07/20/2015
f1_keywords:
- protected
- protected_CSharpKeyword
helpviewer_keywords:
- protected keyword [C#]
ms.assetid: 05ce3794-6675-4025-bddb-eaaa0ec22892
ms.openlocfilehash: f25e692430f876ec384971079d6d0aa2c97e967b
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/09/2018
ms.locfileid: "44197875"
---
# <a name="protected-c-reference"></a>protected（C# 参考）

`protected` 关键字是一个成员访问修饰符。

 > 本页涵盖 `protected` 访问。 `protected` 关键字也属于 [`protected internal`](protected-internal.md) 和 [`private protected`](private-protected.md) 访问修饰符。

受保护成员在其所在的类中可由派生类实例访问。

有关 `protected` 和其他访问修饰符的比较，请参阅[可访问性级别](accessibility-levels.md)。

## <a name="example"></a>示例

只有在通过派生类类型进行访问时，基类的受保护成员在派生类中才是可访问的。 以下面的代码段为例：

[!code-csharp[csrefKeywordsModifiers#11](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsModifiers/CS/csrefKeywordsModifiers.cs#11)]

语句 `a.x = 10` 生成错误，因为它是在静态方法 Main 中生成的，而不是类 B 的实例。

无法保护结构成员，因为无法继承结构。

## <a name="example"></a>示例

在此示例中，`DerivedPoint` 类是从 `Point` 派生的。 因此，可以从派生类直接访问基类的受保护成员。

[!code-csharp[csrefKeywordsModifiers#12](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsModifiers/CS/csrefKeywordsModifiers.cs#12)]  

如果将 `x` 和 `y` 的访问级别更改为 [private](private.md)，编译器将发出错误消息：

`'Point.y' is inaccessible due to its protection level.`

`'Point.x' is inaccessible due to its protection level.`

## <a name="c-language-specification"></a>C# 语言规范

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>请参阅

- [C# 参考](../../../csharp/language-reference/index.md)
- [C# 编程指南](../../../csharp/programming-guide/index.md)
- [C# 关键字](index.md)
- [访问修饰符](access-modifiers.md)
- [可访问性级别](accessibility-levels.md)
- [修饰符](modifiers.md)
- [public](public.md)
- [private](private.md)
- [internal](internal.md)
- [Internal Virtual 关键字的安全问题](https://docs.microsoft.com/en-us/previous-versions/dotnet/netframework-4.0/heyd8kky(v=vs.100))