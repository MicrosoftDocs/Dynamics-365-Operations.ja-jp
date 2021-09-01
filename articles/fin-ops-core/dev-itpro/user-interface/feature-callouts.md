---
title: 機能のコールアウト
description: 機能のコールアウトをトリガーして、ユーザーに新しい機能を認識してもらいましょう。
author: jasongre
ms.date: 05/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2019-5-31
ms.dyn365.ops.version: Platform update 26
ms.openlocfilehash: febdde53463d827eae6436954d27b27908dcc19232722fb9aa608134ab8eecb9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6737819"
---
# <a name="feature-callouts"></a>機能のコールアウト

[!include [banner](../includes/banner.md)]


## <a name="introduction"></a>はじめに
ドキュメントは新機能の説明に役立ちますが、製品の使用中にユーザーがその機能に遭遇した場合は、これらの新機能について認識を高めることも重要です。 その結果、機能のコールアウトをプラットフォームの更新プログラム 26 で使用できます。 機能のコールアウトを使用して、ユーザーに新しい機能を示して、オプションで機能の詳細を知るためのハイパーリンクをユーザーに提供することができます。 

このトピックでは、機能のコールアウトの作成に使用される API について詳しく説明します。   

![ナビゲーション ウィンドウの機能のコールアウトの変更。](./media/cli_featureCallout_noLink.png "プラットフォーム更新プログラム 22 でリリースされたナビゲーション ウィンドウの機能のコールアウトの変更")
  
## <a name="the-got-it-button"></a>"了解" ボタン
機能のコールアウトがトリガーされたら、ユーザは **了解** ボタンをただクリックしてポップアップを閉じることができます。 これにより、この機能コールアウトの状態が個人用設定サブシステムに保存され、特定の機能コールアウトが再度トリガーされるのを防ぎます。 

## <a name="resetting-feature-callouts"></a>機能のコールアウトのリセット
機能コールアウトの状態が個人用設定に保存されている場合、個人用設定をクリアしても以前に閉じたすべての機能コールアウトの状態は削除されません。 代わりに、すべての機能コールアウトをリセットして再び起動するようにする、別のアクションが追加されました。 これらのアクションは、**使用状況データ** ページの **個人用設定** タブ、および **個人設定** ページの **ユーザーごとに管理** タブにあります。   

## <a name="disabling-feature-callouts"></a>機能のコールアウトの無効化 
管理者は必要に応じて、**クライアント パフォーマンス オプション** ページで **機能のコールアウトを有効化** オプションを使用して、環境に対して機能のコールアウトを無効にできます。 
  
## <a name="implementation-details"></a>実装詳細
SystemNotificationsWhatsNewManager クラスには、機能のコールアウトをトリガーするための 2 つのバリアント API が含まれています。 

### <a name="addwhatsnewwithactionlink"></a>AddWhatsNewWithActionLink() 
新しい製品の機能に関連付けられているドキュメントを開くように構成されている [詳細情報] のリンクを含むコントロールに機能のコールアウトを追加します。  

#### <a name="parameters"></a>パラメーター

| パラメーター     | 説明                                                               |
|---------------|---------------------------------------------------------------------------|
| ruleID        | 一意の GUID を生成します。                                                    | 
| title         | (ローカライズ済みの) タイトルを入力します。                                               | 
| bodyText      | (ローカライズ済みの) 説明を入力します。                                         | 
| targetControl | 機能のコールアウトを追加するコントロールの名前を提供します。 | 
| urlLink       | "詳細" リンクをクリックしたときに、新しいタブで開く URL を指定します。 URL が指定されない場合、"詳細" リンクは表示されません。 |


### <a name="addwhatsnew"></a>AddWhatsNew() 
機能のコールアウトを [詳細情報] リンクのないコントロールに追加します。 

#### <a name="parameters"></a>パラメーター

| パラメーター     | 説明                                                               |
|---------------|---------------------------------------------------------------------------|
| ruleID        | 一意の GUID を生成します。                                                    | 
| title         | (ローカライズ済みの) タイトルを入力します。                                               | 
| bodyText      | (ローカライズ済みの) 説明を入力します。                                         | 
| targetControl | 機能のコールアウトを追加するコントロールの名前を提供します。 | 

### <a name="example"></a>例
次のコードスニペットは、*TestStringControl* というコントロールに関連付けられている機能のコールアウトをトリガーします。  

```xpp
public void init() 
{
     super(); 
     
     SystemNotificationsWhatsNewManager::AddWhatsNewWithActionLink(
          MyTestKey, 
          "My title" , 
          "My description", 
          TestStringControl.name(), 
          "https://www.microsoft.com"
     );
}
```

## <a name="notes"></a>摘要
-  複数の機能のコールアウトを一度に 1 ページに表示できます。
-  機能のコールアウトは、コントロールごとに 1 つのみ使用できます。 複数のコールアウトが存在する場合は、最後にトリガーされたものが表示されます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]