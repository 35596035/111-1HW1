# 第1次作業-作業-HW1
>
>學號：109111101
><br />
>姓名：邱韋翔
><br />
>作業撰寫時間：12 (mins，包含程式撰寫時間)
><br />
>最後撰寫文件日期：2022/09/13
>

本份文件包含以下主題：(至少需下面兩項，若是有多者可以自行新增)
- [x]說明內容
- [x]個人認為完成作業須具備觀念

## 說明程式與內容

首先我的想法是根據readme.md檔的提示內容，拉出一個button物件拉到`<div></div>`之間
再改button上的屬性，修改button的ID另外我是有在多修改button物件的高度及寬度好讓按鈕大點
```html
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="Test.aspx.cs" Inherits="_111_1HW1.Test" %>

<!DOCTYPE html>

<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
<meta http-equiv="Content-Type" content="text/html; charset=utf-8"/>
    <title></title>
</head>
<body>
    <form id="form1" runat="server">
        <div>
            <asp:Button ID="btn_Show" runat="server" Text="Button" Height="300px" Width="200px" OnClick="btn_Click" />
        </div>
    </form>
</body>
</html>
```
根據readme.md檔的內容在Page_Load加入可以讓畫面輸出`Hello APP`的字樣，所以我使用
`Response.Write()`來完成
```csharp
        protected void Page_Load(object sender, EventArgs e)
        {
            Response.Write("Hello App");
        }
```
根據readme.md檔的內容點擊button按鈕物件會輸出`Hello Button`字樣，所以我在
btn_Click加入`Response.Write()`來達成
```csharp
        protected void btn_Click(object sender, EventArgs e)
        {
            Response.Write("Hello Button");
        }

```
最後輸出結果是先在螢幕出現`Hello APP`的字樣，隨後按下按鈕`Hello Button`的字樣會直接
加在`Hello APP`後，變成`Hello APPHello Button`


## 個人認為完成作業須具備觀念

我覺得這次作業須先了解到新增按鈕物件的位置，必須先點選Test.aspx檔再點選工具箱
才能看到許多可拖曳物件，找到button物件之後拖曳到`<div></div>`之間
再修改button屬性的ID根據readme.md要求修改btn_Show後，到Test.aspx.cs輸入對應的程式碼，
如輸出就會用到`Reponse.Write()`來完成此次作業

