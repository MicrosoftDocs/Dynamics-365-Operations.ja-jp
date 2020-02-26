---
title: コマース拡張リソースおよびラベル ファイルのローカライズ
description: このトピックでは、POS UI ラベル、POS メッセージ、入庫ラベル、および Commerce Scale Unit または CRT のエラー メッセージを変更する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Retail, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: mumani
ms.search.validFrom: 2018-05-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 7f0f60a3396751e15d167b890c1f3aac25e440de
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004573"
---
# <a name="localize-commerce-extension-resources-and-label-files"></a>コマース拡張リソースおよびラベル ファイルのローカライズ

[!include[banner](../includes/banner.md)]


このトピックでは、販売時点管理 (POS) ユーザー インターフェイス (UI)、POS メッセージ (エラー、警告、および情報)、入庫ラベル、および Commerce Scale Unit または Commerce Runtime のサービス (CRT) のエラー メッセージの点にラベルを変更する方法について説明します。 カスタム エラー メッセージを同じ方法で追加することもできます。 ただし、新しい POS 拡張ラベルの場合は、POS 拡張のローカライズ フレームワークを使用します。

## <a name="pos-labels-and-messages-error-warning-and-information"></a>POS ラベルおよびメッセージ (エラー、警告、および情報)

このセクションでは、既定の文字列を上書きすることによって、POS UI ラベルおよび POS メッセージを変更する方法について説明します。

### <a name="override-pos-ui-labels-and-messages"></a>POS UI ラベルおよびメッセージの上書き

**言語テキスト** ページの言語テキスト エントリを使用して、POS の既定の文字列を上書きすることができます。 POS 文字列を変更するには、次の手順を実行します。

1. コマースにサインインします。
2. **Retail とコマース &gt; チャネル設定 &gt; POS 設定 &gt; POS プロファイル &gt; 言語テキスト**の順に移動します。
3. **言語テキスト**ページの、**POS** タブの **POS 言語テキスト**グリッドで、**追加**ボタンを選択して言語 ID、テキスト ID、および上書きする文字列のテキストを追加します。

    たとえば、POS サインイン ページの**オペレーター ID** フィールドのラベルを、アメリカ英語 (en-us) の**従業員 ID** に変更したいとします。 この場合、**POS 言語テキスト**グリッドで次のエントリを追加します。

    | 言語 ID | テキスト ID | テキスト        |
    |-------------|---------|-------------|
    | ja       | 502     | 従業員 ID |

    > [!NOTE]
    > POS 文字列のテキスト ID を取得する方法の詳細については、次のセクションを参照してください。

4. アクション ウィンドウで、**保存**を選択します。
5. **Retail とコマース &gt; Retail とコマース IT &gt; 配送スケジュール**の順に移動します。
6. **レジスター** (**1090**) ジョブを選択し、**今すぐ実行**を選択します。
7. データをプッシュ後、クラウド POS または Modern POS でログインし、変更済のラベルを表示します。

### <a name="get-the-text-id-for-pos-strings"></a>POS 文字列のテキスト ID を取得します

POS 文字列のテキスト ID を取得するには、デバッグ モードで Retail ソフトウェア開発キット (SDK) を使用して、POS を実行する必要があります。 POS では、テキスト ID を文字列 ID と呼びます。

1. Microsoft Visual Studio 2015 を管理者モードで起動します。
2. **ModernPOS** ソリューションを **…\\RetailSDK\\POS** から開きます。
3. **ソリューション構成**プロパティを**デバッグ**に、**ソリューション プラットフォーム**プロパティを **x86** に、および**配置**プロパティを**ローカル コンピューター**に設定します。
4. ソリューションをコンパイル、およびビルドしてから、**配置\>ローカル コンピューター**を選択します。
5. POS 配置後、オペレーター ID およびパスワードを使いログインします。
6. POS ウィンドウの右上で**設定**ボタンを選択します。
7. **設定**ページの**開発者モード**で、**開発者モード**オプションを**はい**に設定します。
8. **文字列 ID の表示**オプションを**はい**に設定します。
9. POS からサインアウトし、再度サインインします。 POS には、すべてのラベルとメッセージの前に文字列 ID が表示されるようになります。 

### <a name="troubleshooting"></a>トラブルシューティング

**開発者モード**オプションが POS の**設定**ページに表示されない場合は、デバッグ モードで動作していることを確認してください。 **pos.js** ファイルを開き、**Config.isDebugMode** が **true** に設定されていることを確認します。 **false** に設定されている場合、値を **true** に変更し、再度 POS を配置します。 **pos.js** ファイル内で **Config.isDebugMode** が見つからない場合。 JavaScript コンソールで **Commerce.Helpers.DeveloperModeHelper.setDeveloperMode(true);** コマンドを実行して、開発者モードを起動します。 F12 を押下して 開発者コマンドツールを起動し、 **コンソール** タブを選択して JavaScript コンソールを開きます。

> [!IMPORTANT]
> クイック テストを行い、文字列 ID を取得するために、pos.js ファイル**のみ**を編集する必要があります。 そのような場合、ファイルを編集した後に、変更内容を元に戻す必要があります。 Microsoft のコア ファイルに加えた変更は展開中に上書きされます。 そのため、変更は失われます。 また、将来のバージョンでは、pos.js ファイルの編集をサポートしない可能性があります。

## <a name="error-messages-or-receipt-strings"></a>エラー メッセージまたは入庫文字列

このセクションでは、既定の文字列を上書きすることによってエラー メッセージ、または入庫文字列を変更する方法について説明します。 新規、カスタム エラー メッセージ、または入庫文字列を追加する方法についても説明します。

### <a name="override-error-messages-or-receipt-strings"></a>エラー メッセージまたは入庫文字列を上書きする

1. コマースにサインインします。
2. **Retail とコマース \> チャネル設定 \> POS 設定 \> POS プロファイル \> 言語テキスト**の順に移動します。
3. **言語テキスト** ページで、**追加**ボタンをクリックして、上書きする文字列の言語 ID、テキスト ID、およびテキストを追加します。

    たとえば、サインイン中にユーザーが間違ったユーザー名またはパスワードを入力すると、POS に次のエラー メッセージが表示されます: 「ユーザー名またはパスワードが認識されませんでした。」 もう一度やり直してください。」 英語 (US) では、メッセージを「有効なユーザー名またはパスワードを入力してください」に変更します。 この場合、**言語テキスト** グリッドで次のエントリを追加します。

    | 言語 ID | テキスト ID                                                              | テキスト                                     |
    |-------------|----------------------------------------------------------------------|------------------------------------------|
    | ja       | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidAuthenticationCredentials | 有効なユーザー名またはパスワードを入力してください |

    > [!NOTE]
    > エラー メッセージのテキスト ID、および入庫文字列を取得する方法の詳細については、次のセクションを参照してください。

4. アクション ウィンドウで、**保存**を選択します。
5. **Retail とコマース \> Retail とコマース IT \> 配送スケジュール**の順に移動します。
6. **レジスター** (**1090**) ジョブを選択し、**今すぐ実行**を選択します。

### <a name="get-the-text-id-for-messages-or-receipt-strings"></a>メッセージまたは入庫文字列のテキスト ID を取得する

1. **…\\RetailSDK\\ドキュメント\\リソース**に移動します。
2. Visual Studio で、次のリソース ファイルのいずれかを開きます。

    - **エラー メッセージを変更するには:** RuntimeExceptionMessages.resx
    - **入力された文字列の変更:** RuntimeReceiptMessages.resx

    リソース ファイル内のすべてのメッセージについて、Visual Studio は名前と値を表示します。

3. **値**列で、変更するテキストを検索します。
4. その値に対応する名前をコピーします。 この名前をテキスト ID として**言語テキスト** グリッドに入力します。

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
                        LocalizedMessage = "My new message in US English.",
                        LocalizedMessageParameters = new object[] { }
                    };
```
