---
title: Store Commerce の設定とインストールに関する問題のトラブルシューティング
description: この記事では、Microsoft Dynamics 365 Commerce Store Commerce アプリの設定およびインストールの問題に関するトラブルシューティングの方法について説明します。
author: mugunthanm
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 8af2c476ced05fc159a53131f8b51ad914a6c7c3
ms.sourcegitcommit: c271b2edc4bf777f7194b09139ccbd174a359c75
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/16/2022
ms.locfileid: "9168950"
---
# <a name="troubleshoot-store-commerce-setup-and-installation-issues"></a>Store Commerce の設定とインストールに関する問題のトラブルシューティング

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce Store Commerce アプリの設定およびインストールの問題に関するトラブルシューティングの方法について説明します。

## <a name="i-cant-activate-the-app-and-i-receive-a-connectivity-error-message"></a>アプリを有効にできず、接続エラー メッセージが表示される

有効なクラウド販売時点管理 (CPOS) URLを入力すると、次のような接続エラー メッセージが表示される場合があります。

> 接続エラーが発生しました。デバイスが CPOS に接続できません。 入力した CPOS URL にいくつかの問題がある場合があります。

この場合、URL に誤字がないか確認するか、CPOS がオフラインのため到達できないかどうかを判断します。

また、Cloud Scale Unit (CSU) バージョンが 10.0.25 (9.35.\*.\*) 以降であることを確認します。 Store Commerce アプリを使用するには、CPOS バージョン 10.0.25 以降が必要です。

## <a name="i-cant-install-the-app-because-modern-pos-is-already-installed"></a>Modern POS が既にインストールされているので、アプリをインストールできない

インストール時、次の例のようなエラー メッセージが表示される場合があります。

> この製品 (Modern POS) のバージョン (9.\*.\*.\*) は、以前にレガシ インストーラーを通じてインストールされています。

エラーを修正するには、コンピューターのすべてのユーザーの Modern 販売時点管理 (MPOS) アプリをアンインストールしてからやり直す必要があります。 次の PowerShell コマンドを実行することで、すべてのユーザーの MPOS が削除されたかどうかを確認できます。

```PowerShell
Get-AppxPackage | Where-Object {$_.PackageFullName -like "Microsoft.Dynamics.*.Pos"} | Remove-AppxPackage -Allusers
```

## <a name="i-cant-activate-the-app-because-of-an-invalid-url-or-an-error-state"></a>無効な URL またはエラー状態によりアプリを有効にできない

入力した CPOS URL が無効で、変更したい場合、または、有効化の際に Store Commerce アプリがエラー状態にある場合は、アプリをリセットしてプロセスを再開できます。 Store Commerce アプリでは、有効な CPOS URL のみ保存されます。

Store Commerce アプリをリセットするには、以下の手順を実行します。

1. Windowsvの **スタート** メニューで、アプリを選択したまま (あるいは右クリックして) 、それから **詳細 \>アプリの設定** を選択します。
2. アプリ設定ページを **リセット** ボタンが見つかるまで下にスクロールします。
3. **リセット** を選択します。 次に、表示されたらアプリのリセットを確認します。
