# SOLID 原則
SOLID 原則是物件導向程式（OOP）的 5 個基本原則，遵守這些原則的程式碼會更容易維護、擴充與修改。

## 目錄
- [簡介](#簡介)
- [單一職責](#單一職責)
- [開放封閉](#開放封閉)
- [里氏替換](#里氏替換)
- [介面隔離](#介面隔離)
- [依賴反轉](#依賴反轉)
- [參考資料](#參考資料)

> [回到主頁面](../README.md#文件)

---

# 簡介
|字母|代表|基本概念|
|:-:|:-:|-|
|S|[單一職責 SRP](#單一職責)|物件、函式和方法應該僅具有一種單一功能。|
|O|[開放封閉 OCP](#開放封閉)|模組、方法和類別應對於擴充是開放的，對於修改是封閉的。|
|L|[里氏替換 LSP](#里氏替換)|程式中的物件應該可以在不改變程式正確性的前提下，被它的子類所替換。|
|I|[介面隔離 ISP](#介面隔離)|多個特定客戶端介面要好過於一個廣泛用途的介面。|
|D|[依賴反轉 DIP](#依賴反轉)|高層模組不應該依賴於低層模組，兩者皆應該依賴於抽象介面。|

筆者個人認爲這 5 項原則的重要程度爲：
- 非常重要
  - S-單一職責
  - D-依賴反轉
- 重要
  - O-開放封閉
  - I-介面隔離
- 一般
  - L-里氏替換

# 單一職責
> Single responsibility principle (SRP)

- 物件、函式和方法應該僅具有一種單一功能。

# 開放封閉
> Open–closed principle (OCP)

- 模組、方法和類別應對於擴充是開放的，對於修改是封閉的。
  - 意指：應該將軟體設計成不對其修改就能擴展功能。

# 里氏替換
> Liskov substitution principle (LSP)

- 程式中的物件應該可以在不改變程式正確性的前提下，被它的子類所替換。

# 介面隔離
> Interface segregation principle (ISP)

- 多個特定客戶端介面要好過於一個廣泛用途的介面。

# 依賴反轉
> Dependency inversion principle (DIP)

- 高層模組不應該依賴於低層模組，兩者皆應該依賴於抽象介面。
- 抽象介面不應該依賴於具體實現。而具體實現則應該依賴於抽象介面。

## 範例
### 沒有依賴反轉的一般寫法：
```cs
// 沒有依賴反轉的一般寫法。

class Engine
{
    void Start()
    {
        // Some code here.
    }
}

class Car
{
    // 高層模組「Car」直接依賴於低層模組「Engine」。
    Engine MyEngine = new Engine();
    
    // Some code here.
}
```

### 依賴反轉的基本寫法：
```cs
// 依賴反轉的基本寫法。

interface EngineInterface
{
    void Start();
}

// 低層模組「Engine」繼承並實作了介面「EngineInterface」。
class Engine : EngineInterface
{
    void Start()
    {
        // Some code here.
    }
}

class Car
{
    // 高層模組「Car」不直接依賴於低層模組「Engine」，而是依賴於介面「EngineInterface」。
    EngineInterface MyEngine = new Engine();
    
    // Some code here.
}
```

### 依賴反轉的進階寫法：
```cs
// 依賴反轉的進階寫法。

interface EngineInterface
{
    void Start();
}

class Engine : EngineInterface
{
    void Start()
    {
        // Some code here.
    }
}

class Car
{
    EngineInterface MyEngine = null;
    
    // 使用依賴注入（Dependency Injection，DI）的方式實現控制反轉（Inversion of Control，IoC）。
    // 將低層模組「Engine」在高層模組「Car」之外實例化後，才透過建構子傳入「Car」。
    Car(EngineInterface engine)
    {
        MyEngine = engine;
    }
    
    // Some code here.
}

// 實際呼叫「Car」時：
Engine V8Engine = new Engine();
Car MySuperCar = new Car(V8Engine);
```
# 參考資料
- 無瑕的程式碼（Robert C. Martin, Clean Code）
- [我該學會SOLID嗎?](https://medium.com/@f40507777/%E6%88%91%E8%A9%B2%E5%AD%B8%E6%9C%83solid%E5%97%8E-4e73887c9156)
- [物件導向設計原則—SOLID](https://ithelp.ithome.com.tw/articles/10191553)
- [使人瘋狂的 SOLID 原則：目錄](https://medium.com/%E7%A8%8B%E5%BC%8F%E6%84%9B%E5%A5%BD%E8%80%85/%E4%BD%BF%E4%BA%BA%E7%98%8B%E7%8B%82%E7%9A%84-solid-%E5%8E%9F%E5%89%87-%E7%9B%AE%E9%8C%84-b33fdfc983ca)
- [物件導向程式設計基本原則 - SOLID](https://skyyen999.gitbooks.io/-study-design-pattern-in-java/content/oodPrinciple.html)
