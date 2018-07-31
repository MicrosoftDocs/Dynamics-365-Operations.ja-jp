---
title: "Retail 拡張リソースおよびラベル ファイルのローカライズ"
description: "このトピックでは、POS UI ラベル、POS メッセージ、入庫ラベル、および Retail サーバーまたは CRT のエラー メッセージを変更する方法について説明します。 Retail サーバーまたは CRT のカスタム エラー メッセージを追加する方法についても説明します。"
author: mugunthanm
manager: AnnBe
ms.date: 07/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Developer
ms.reviewer: margoc
ms.search.scope: Retail, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: mumani
ms.search.validFrom: 2018-05-31
ms.dyn365.ops.version: 8.0.1
ms.translationtype: HT
ms.sourcegitcommit: f2e3a40f58b57785079e1940b2d24a3598a3ad1b
ms.openlocfilehash: ec2806b70830ad3708e668ee6c1f192bec518b26
ms.contentlocale: ja-jp
ms.lasthandoff: 07/09/2018

---

# <a name="localize-retail-extension-resources-and-label-files"></a>Retail 拡張リソースおよびラベル ファイルのローカライズ

[!include[banner](../includes/banner.md)]


このトピックでは、販売時点管理 (POS) ユーザー インターフェイス (UI)、POS メッセージ (エラー、警告、および情報)、入庫ラベル、および Retail サーバーまたは Commerce Runtime のサービス (CRT) のエラー メッセージの点にラベルを変更する方法について説明します。 Retail サーバーまたは CRT のカスタム エラー メッセージを、同じ方法で追加することもできます。 ただし、新しい POS 拡張ラベルの場合は、POS 拡張のローカライズ フレームワークを使用します。

このトピックは、Microsoft Dynamics 365 for Finance and Operations 7.2 最新の更新プログラムと、Microsoft Dynamics 365 for Retail 7.2 最新の更新プログラム、およびそれ以降のバージョンに適用可能です。

## <a name="retail-pos-labels-and-messages-error-warning-and-information"></a>Retail POS ラベルおよびメッセージ (エラー、警告、および情報)

このセクションでは、既定の文字列を上書きすることによって、POS UI ラベルおよび POS メッセージを変更する方法について説明します。

### <a name="override-pos-ui-labels-and-messages"></a>POS UI ラベルおよびメッセージの上書き

**言語テキスト** ページの言語テキスト エントリを使用して、POS の既定の文字列を上書きすることができます。 POS 文字列を変更するには、次の手順を実行します。

1. Retail または Finance and Operations へのサインイン
2. **小売 &gt; チャネル設定 &gt; POS 設定 &gt; POS プロファイル &gt; 言語テキスト**の順に移動します。
3. **言語テキスト**ページの、**POS** タブの **POS 言語テキスト**グリッドで、**追加**ボタンを選択して言語 ID、テキスト ID、および上書きする文字列のテキストを追加します。

    たとえば、POS サインイン ページの**オペレーター ID** フィールドのラベルを、アメリカ英語 (en-us) の**従業員 ID** に変更したいとします。 この場合、**POS 言語テキスト**グリッドで次のエントリを追加します。

    | 言語 ID | テキスト ID | テキスト        |
    |-------------|---------|-------------|
    | ja       | 502     | 従業員 ID |

    > [!NOTE]
    > POS 文字列のテキスト ID を取得する方法の詳細については、次のセクションを参照してください。

4. アクション ウィンドウで、**保存**を選択します。
5. **小売 &gt; 小売 IT &gt; 配送スケジュール**の順に移動します。
6. **レジスター** (**1090**) ジョブを選択し、**今すぐ実行**を選択します。
7. データをプッシュ後、クラウド POS または Modern POS でログインし、変更済のラベルを表示します。

### <a name="get-the-text-id-for-pos-strings"></a>POS 文字列のテキスト ID を取得します

POS 文字列のテキスト ID を取得するには、デバッグ モードで Retail ソフトウェア開発キット (SDK) を使用して、POS を実行する必要があります。 POS では、テキスト ID を文字列 ID と呼びます。

1. 管理者モードで Microsoft Visual Studio 2015 を起動します。
2. **ModernPOS** ソリューションを **…\\RetailSDK\\POS** から開きます。
3. **ソリューション構成**プロパティを**デバッグ**に、**ソリューション プラットフォーム**プロパティを **x86** に、および**配置**プロパティを**ローカル コンピューター**に設定します。
4. ソリューションをコンパイル、およびビルドしてから、**配置\>ローカル コンピューター**を選択します。
5. POS 配置後、オペレーター ID およびパスワードを使いログインします。
6. POS ウィンドウの右上で**設定**ボタンを選択します。
7. **設定**ページの**開発者モード**で、**開発者モード**オプションを**はい**に設定します。
8. **文字列 ID の表示**オプションを**はい**に設定します。
9. POS からサインアウトし、再度サインインします。 POS には、すべてのラベルとメッセージの前に文字列 ID が表示されるようになります。 

### <a name="troubleshooting"></a>トラブルシューティング

**開発者モード**オプションが POS の**設定**ページに表示されない場合は、デバッグ モードで動作していることを確認してください。 **pos.js** ファイルを開き、**Config.isDebugMode** が **true** に設定されていることを確認します。 **false** に設定されている場合、値を **true** に変更し、再度 POS を配置します。

> [!IMPORTANT]
> クイック テストを行い、文字列 ID を取得するために、pos.js ファイル**のみ**を編集する必要があります。 そのような場合、ファイルを編集した後に、変更内容を元に戻す必要があります。 Microsoft のコア ファイルに加えた変更は展開中に上書きされます。 そのため、変更は失われます。 また、将来のバージョンでは、pos.js ファイルの編集をサポートしない可能性があります。

## <a name="retail-server-or-crt-error-messages-or-receipt-strings"></a>Retail サーバーや CRT エラー メッセージ、または入庫文字列

このセクションでは、既定の文字列を上書きすることによって Retail サーバーまたは CRT エラー メッセージ、または入庫文字列を変更する方法について説明します。 新規、Retail サーバーまたは CRT のカスタム エラー メッセージ、または入庫文字列を追加する方法についても説明します。

### <a name="override-retail-server-or-crt-error-messages-or-receipt-strings"></a>Retail サーバーや CRT エラー メッセージ、または入庫文字列を上書き

1. Retail または Finance and Operations へのサインイン
2. **小売 \> チャネル設定 \> POS 設定 \> POS プロファイル \> 言語テキスト**の順に移動します。
3. **言語テキスト**ページの、**Retail サーバー**タブの **Retail サーバー言語テキスト**グリッドで、**追加**ボタンをクリックして言語 ID、テキスト ID、および上書きする文字列のテキストを追加します。

    たとえば、サインイン中にユーザーが間違ったユーザー名またはパスワードを入力すると、POS に次のエラー メッセージが表示されます: 「ユーザー名またはパスワードが認識されませんでした。」 もう一度やり直してください。」 英語 (US) では、メッセージを「有効なユーザー名またはパスワードを入力してください」に変更します。 この場合、**Retail サーバー 言語テキスト**グリッドで次のエントリを追加します。

    | 言語 ID | テキスト ID                                                              | テキスト                                     |
    |-------------|----------------------------------------------------------------------|------------------------------------------|
    | ja       | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidAuthenticationCredentials | 有効なユーザー名またはパスワードを入力してください |

    > [!NOTE]
    > Retail サーバーまたは CRT エラー メッセージのテキスト ID、および入庫文字列を取得する方法の詳細については、次のセクションを参照してください。

4. アクション ウィンドウで、**保存**を選択します。
5. **小売 \> 小売 IT \> 配送スケジュール**の順に移動します。
6. **レジスター** (**1090**) ジョブを選択し、**今すぐ実行**を選択します。

### <a name="get-the-text-id-for-retail-server-or-crt-messages-or-receipt-strings"></a>Retail サーバーまたは CRT メッセージ、または入庫文字列のためのテキスト ID を取得します。

1. **…\\RetailSDK\\ドキュメント\\リソース**に移動します。
2. Visual Studio で、次のリソース ファイルのいずれかを開きます。

    - **Retail サーバーまたは CRT エラー メッセージを変更する:** RuntimeExceptionMessages.resx
    - **入庫文字列の変更:** RuntimeReceiptMessages.resx

    リソース ファイル内のすべてのメッセージについて、Visual Studio は名前と値を表示します。

3. **値**列で、変更するテキストを検索します。
4. その値に対応する名前をコピーします。 この名前をテキストID として **Retail サーバー言語テキスト** グリッドに入力します。

### <a name="add-custom-retail-server-or-crt-error-messages-or-receipt-strings"></a>カスタム Retail サーバーまたは CRT エラー メッセージ、または入庫文字列を追加

新しい Retail サーバーまたは CRT エラー メッセージ、または、新しい入庫文字列を **Retail サーバー言語テキスト** グリッドに追加することもできます。 この方法で、コード内のハードコーディングのすべての代わりにローカライズをサポートします。

> [!IMPORTANT]
> すべてのメッセージのテキスト ID は **Microsoft\_Dynamics\_Commerce\_** から始まる必要があります。

たとえば、アメリカ英語 (en-us) と英国英語 (en-uk) で新しい例外メッセージを追加したいとします。 この場合、**Retail サーバー言語テキスト**グリッドでの次のエントリに類似したエントリを追加します。

| 言語 ID | テキスト ID                                 | テキスト                    |
|-------------|-----------------------------------------|-------------------------|
| ja       | Microsoft_Dynamics_Commerce_CustomId1 | アメリカ英語での新しいメッセージ |
| en-uk       | Microsoft_Dynamics_Commerce_CustomId1 | 英国英語での新しいメッセージ |

> [!NOTE]
> この例では、**CustomId1** が新しいメッセージのテキスト ID です。 使用したい任意のテキスト ID を使用することができます。ただし、**Microsoft_Dynamics_Commerce_** で始まる場合に限ります

次の例では、この新しいメッセージを CRT 拡張コードで使用する方法を示します。

```C#
throw new CommerceException("Microsoft_Dynamics_Commerce_CustomId1", ExceptionSeverity.Warning, null, "Custom error");
```

