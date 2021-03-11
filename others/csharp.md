# C#
## 目錄
- [委派（delegate）與 Lambda 運算子](#委派delegate與-Lambda-運算子)

> [回到主頁面](../README.md#文件)

---

# 委派（delegate）與 Lambda 運算子

```cs
class Demo
{
  // 委派。
  delegate void MyAction();
  
  void Main()
  {
    MyAction act = null;
    
    // 正統的完整寫法。
    act = new MyAction(A);
    act();
    
    // 簡化的寫法，語法糖。
    act = B;
    act();
    
    // 使用 Lambda 運算子達成匿名方法。
    act = () => MessageBox.Show("C");
    act();
    
    // 多行的匿名方法。
    act = () => 
    {
      MessageBox.Show("D1");
      MessageBox.Show("D2");
      MessageBox.Show("D3");
    };
    act();
  }
      
  void A()
  {
    Message.Show("A");
  }
  
  void B()
  {
    Message.Show("B");
  }
}
```

## 參考資料
- [委派 - C# 程式設計手冊 | Microsoft Docs](https://docs.microsoft.com/zh-tw/dotnet/csharp/programming-guide/delegates/)
- [delegate 運算子 - C# 參考 | Microsoft Docs](https://docs.microsoft.com/zh-tw/dotnet/csharp/language-reference/operators/delegate-operator)
- [=> 運算子 - C# 參考 | Microsoft Docs](https://docs.microsoft.com/zh-tw/dotnet/csharp/language-reference/operators/lambda-operator)
- [C#雜記 — 委派(Delegate)、FUNC<>、ACTION<> | by 莊創偉 | Medium](https://ad57475747.medium.com/c-%E9%9B%9C%E8%A8%98-%E5%A7%94%E6%B4%BE-delegate-func-action-4b3191c7a131)
- [茅塞頓開的一晚-Func 委派+匿名方法+lambda | 我的Coding之路 - 點部落](https://dotblogs.com.tw/lastsecret/2010/06/26/16201)
