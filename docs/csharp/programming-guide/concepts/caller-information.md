---
title: 调用方信息 (C#)
ms.date: 07/20/2015
ms.assetid: ffad3d24-2fb7-4641-9124-53b5bc91d339
ms.openlocfilehash: 048e91ad337f74ef04a2a03412a44a0be0ef9506
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/08/2018
ms.locfileid: "44212446"
---
# <a name="caller-information-c"></a>调用方信息 (C#)
通过使用调用方信息特性，可获取有关方法的调用方的信息。 可以获取源代码的文件路径、源代码中的行号和调用方的成员名称。 此信息有助于跟踪、调试和创建诊断工具。  
  
 若要获取此信息，可以使用应用于可选参数的特性，每个特性都具有默认值。 下表列出在 <xref:System.Runtime.CompilerServices?displayProperty=nameWithType> 命名空间中定义的调用方信息特性：  
  
|特性|描述|类型|  
|---|---|---|  
|<xref:System.Runtime.CompilerServices.CallerFilePathAttribute>|包含调用方的源文件的完整路径。 这是编译时的文件路径。|`String`|  
|<xref:System.Runtime.CompilerServices.CallerLineNumberAttribute>|源文件中调用方法的行号。|`Integer`|  
|<xref:System.Runtime.CompilerServices.CallerMemberNameAttribute>|调用方的方法或属性名称。 请参阅本主题后面的[成员名称](#MEMBERNAMES)。|`String`|  
  
## <a name="example"></a>示例  
 下面的示例演示如何使用调用方信息特性。 每次调用 `TraceMessage` 方法时，调用方信息将替换为可选参数的变量。  
  
```csharp  
public void DoProcessing()  
{  
    TraceMessage("Something happened.");  
}  
  
public void TraceMessage(string message,  
        [System.Runtime.CompilerServices.CallerMemberName] string memberName = "",  
        [System.Runtime.CompilerServices.CallerFilePath] string sourceFilePath = "",  
        [System.Runtime.CompilerServices.CallerLineNumber] int sourceLineNumber = 0)  
{  
    System.Diagnostics.Trace.WriteLine("message: " + message);  
    System.Diagnostics.Trace.WriteLine("member name: " + memberName);  
    System.Diagnostics.Trace.WriteLine("source file path: " + sourceFilePath);  
    System.Diagnostics.Trace.WriteLine("source line number: " + sourceLineNumber);  
}  
  
// Sample Output:  
//  message: Something happened.  
//  member name: DoProcessing  
//  source file path: c:\Users\username\Documents\Visual Studio 2012\Projects\CallerInfoCS\CallerInfoCS\Form1.cs  
//  source line number: 31  
```  
  
## <a name="remarks"></a>备注  
 你必须为每个可选参数指定显式默认值。 不能将调用方信息特性应用于未指定为可选的参数。  
  
 调用方信息特性不会使参数成为可选参数。 相反，它们会在忽略此参数时影响传入的默认值。  
  
 在编译时，调用方信息值将作为文本传入中间语言 (IL)。 与异常的 <xref:System.Exception.StackTrace%2A> 属性的结果不同，这些结果不受模糊处理的影响。  
  
 你可显式提供可选参数来控制调用方信息或隐藏调用方信息。  
  
###  <a name="MEMBERNAMES"></a>成员名称  
 可以使用 `CallerMemberName` 特性来避免将成员名称指定为所调用的方法的 `String` 参数。 通过使用这种技术，可以避免“重命名重构”不更改 `String` 值的问题。 此好处对于以下任务特别有用：  
  
-   使用跟踪和诊断例程。  
  
-   在绑定数据时实现 <xref:System.ComponentModel.INotifyPropertyChanged> 接口。 此接口允许对象的属性通知绑定控件该属性已更改，以便此控件能够显示更新的信息。 如果没有 `CallerMemberName` 特性，则必须将属性名称指定为文本。  
  
 以下图表显示在使用 `CallerMemberName` 特性时返回的成员名称。  
  
|调用发生中|成员名称结果|  
|-------------------------|------------------------|  
|方法、属性或事件|从中发起调用的方法、属性或事件的名称。|  
|构造函数|字符串“.ctor”|  
|静态构造函数|字符串“.cctor”|  
|析构函数|字符串“Finalize”|  
|用户定义的运算符或转换|为成员生成的名称，例如，“op_Addition”。|  
|特性构造函数|要应用特性的成员的名称。 如果该特性是成员中的任何元素（如参数、返回值或泛型参数），则此结果是与该元素关联的成员的名称。|  
|无包含的成员（例如，程序集级别或应用于类型的特性）|可选参数的默认值。|  
  
## <a name="see-also"></a>请参阅

- [特性 (C#)](../../../csharp/programming-guide/concepts/attributes/index.md)  
- [通用特性 (C#)](../../../csharp/programming-guide/concepts/attributes/common-attributes.md)  
- [命名参数和可选参数](../../../csharp/programming-guide/classes-and-structs/named-and-optional-arguments.md)  
- [编程概念 (C#)](../../../csharp/programming-guide/concepts/index.md)
