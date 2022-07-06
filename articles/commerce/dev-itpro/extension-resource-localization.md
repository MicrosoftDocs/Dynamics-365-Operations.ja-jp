---
title: Commerce 拡張リソースおよびラベル ファイルのローカライズ
description: この記事では、POS UI ラベル、POS メッセージ、入庫ラベル、および Commerce Scale Unit または CRT のエラー メッセージを変更する方法について説明します。
author: mugunthanm
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.search.industry: retail
ms.author: mumani
ms.search.validFrom: 2018-05-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: c89832e2b2b66a7723c0b21d457223ed076b8cff
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892638"
---
# <a name="localize-commerce-extension-resources-and-label-files"></a>Commerce 拡張リソースおよびラベル ファイルのローカライズ

[!include[banner](../includes/banner.md)]


この記事では、販売時点管理 (POS) ユーザー インターフェイス (UI)、POS メッセージ (エラー、警告、および情報)、入庫ラベル、および Commerce Scale Unit または Commerce Runtime のサービス (CRT) のエラー メッセージの点にラベルを変更する方法について説明します。 カスタム エラー メッセージを同じ方法で追加することもできます。 ただし、新しい POS 拡張ラベルの場合は、POS 拡張のローカライズ フレームワークを使用します。

## <a name="pos-labels-and-messages-error-warning-and-information"></a>POS ラベルおよびメッセージ (エラー、警告、および情報)

このセクションでは、既定の文字列を上書きすることによって、POS UI ラベルおよび POS メッセージを変更する方法について説明します。

### <a name="override-pos-ui-labels-and-messages"></a>POS UI ラベルおよびメッセージの上書き

**言語テキスト** ページの言語テキスト エントリを使用して、POS の既定の文字列を上書きすることができます。 POS 文字列を変更するには、次の手順を実行します。

1. コマースにサインインします。
2. **Retail とコマース &gt; チャネル設定 &gt; POS 設定 &gt; POS プロファイル &gt; 言語テキスト** の順に移動します。
3. **言語テキスト** ページの、**POS** タブの **POS 言語テキスト** グリッドで、**追加** ボタンを選択して言語 ID、テキスト ID、および上書きする文字列のテキストを追加します。

    たとえば、POS サインイン ページの **オペレーター ID** フィールドのラベルを、アメリカ英語 (en-us) の **従業員 ID** に変更したいとします。 この場合、**POS 言語テキスト** グリッドで次のエントリを追加します。

    | 言語 ID | テキスト ID | テキスト        |
    |-------------|---------|-------------|
    | ja       | 502     | 従業員 ID |

    > [!NOTE]
    > POS 文字列のテキスト ID を取得する方法の詳細については、次のセクションを参照してください。

4. アクション ウィンドウで、**保存** を選択します。
5. **Retail とコマース &gt; Retail とコマース IT &gt; 配送スケジュール** の順に移動します。
6. **レジスター** (**1090**) ジョブを選択し、**今すぐ実行** を選択します。
7. データをプッシュ後、クラウド POS または Modern POS でログインし、変更済のラベルを表示します。

### <a name="get-the-text-id-for-pos-strings"></a>POS 文字列のテキスト ID を取得します

POS 文字列のテキスト ID を取得するには、最新の POS/Cloud POS アプリケーションを開きます。 F12 を押下して 開発者コマンドツールを起動し、 **コンソール** タブを選択して JavaScript コンソールを開きます。 JavaScript コンソールで **Commerce.Helpers.DeveloperModeHelper.setDeveloperMode(true);** コマンドを実行して、開発者モードを起動します。

JavaScript コンソールで開発者モードを有効にした後、**開発者モード** の下にある POS の **設定** ページに移動し、**開発者モード** を **はい** に設定します。 **文字列 ID の表示** を **はい** に設定します。 POS からサインアウトし、再度サインインします。 POS には、すべてのラベルとメッセージの前に文字列 ID が表示されるようになります。


## <a name="error-messages-or-receipt-strings"></a>エラー メッセージまたは入庫文字列

このセクションでは、既定の文字列を上書きすることによってエラー メッセージ、または入庫文字列を変更する方法について説明します。 新規、カスタム エラー メッセージ、または入庫文字列を追加する方法についても説明します。

### <a name="override-error-messages-or-receipt-strings"></a>エラー メッセージまたは入庫文字列を上書きする

1. コマースにサインインします。
2. **Retail とコマース \> チャネル設定 \> POS 設定 \> POS プロファイル \> 言語テキスト** の順に移動します。
3. **言語テキスト** ページで、**追加** ボタンをクリックして、上書きする文字列の言語 ID、テキスト ID、およびテキストを追加します。

    たとえば、サインイン中にユーザーが間違ったユーザー名またはパスワードを入力すると、POS に次のエラー メッセージが表示されます: 「ユーザー名またはパスワードが認識されませんでした。」 もう一度やり直してください。」 英語 (US) では、メッセージを「有効なユーザー名またはパスワードを入力してください」に変更します。 この場合、**言語テキスト** グリッドで次のエントリを追加します。

    | 言語 ID | テキスト ID                                                              | テキスト                                     |
    |-------------|----------------------------------------------------------------------|------------------------------------------|
    | ja       | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidAuthenticationCredentials | 有効なユーザー名またはパスワードを入力してください |

    > [!NOTE]
    > エラー メッセージのテキスト ID、および入庫文字列を取得する方法の詳細については、次のセクションを参照してください。

4. アクション ウィンドウで、**保存** を選択します。
5. **Retail とコマース \> Retail とコマース IT \> 配送スケジュール** の順に移動します。
6. **レジスター** (**1090**) ジョブを選択し、**今すぐ実行** を選択します。

### <a name="get-the-text-id-for-messages-or-receipt-strings"></a>メッセージまたは入庫文字列のテキスト ID を取得する

1. **…\\RetailSDK\\ドキュメント\\リソース** に移動します。
2. Visual Studio で、次のリソース ファイルのいずれかを開きます。

    - **エラー メッセージを変更するには:** RuntimeExceptionMessages.resx
    - **入力された文字列の変更:** RuntimeReceiptMessages.resx

    リソース ファイル内のすべてのメッセージについて、Visual Studio は名前と値を表示します。

3. **値** 列で、変更するテキストを検索します。
4. その値に対応する名前をコピーします。 この名前をテキスト ID として **言語テキスト** グリッドに入力します。

### <a name="add-custom-error-messages-or-receipt-strings"></a>カスタム エラー メッセージまたは入庫文字列を追加する

新しいエラー メッセージまたは新しい入庫文字列を、**言語テキスト** ページで追加することもできます。 この方法で、コード内のハードコーディングのすべての代わりにローカライズをサポートします。

> [!IMPORTANT]
> すべてのメッセージのテキスト ID は **Microsoft\_Dynamics\_Commerce\_** から始まる必要があります。

たとえば、アメリカ英語 (en-us) と英国英語 (en-uk) で新しい例外メッセージを追加したいとします。 この場合、**言語テキスト** ページでの次のエントリに類似したエントリを追加します。

| 言語 ID | テキスト ID                                 | テキスト                    |
|-------------|-----------------------------------------|-------------------------|
| ja       | Microsoft_Dynamics_Commerce_CustomId1 | アメリカ英語での新しいメッセージ |
| en-uk       | Microsoft_Dynamics_Commerce_CustomId1 | 英国英語での新しいメッセージ |

> [!NOTE]
> この例では、**CustomId1** が新しいメッセージのテキスト ID です。 使用したい任意のテキスト ID を使用することができます。ただし、**Microsoft_Dynamics_Commerce_** で始まる場合に限ります

次の例では、この新しいメッセージを CRT 拡張コードで使用する方法を示します。

```C#
throw new CommerceException("Microsoft_Dynamics_Commerce_CustomId1", ExceptionSeverity.Warning, null, "Custom error")
                    {
                        LocalizedMessage = "My new message in US English.",
                        LocalizedMessageParameters = new object[] { }
                    };
```


[!INCLUDE[footer-include](../../includes/footer-banner.md)]