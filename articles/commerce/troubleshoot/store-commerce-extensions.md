---
title: Store Commerce 拡張機能の問題のトラブルシューティング
description: この記事では、Microsoft Dynamics 365 Commerce Store Commerce アプリの拡張機能の問題に関するトラブルシューティングの方法について説明します。
author: mugunthanm
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: b440183e255e05c4f93a4f11106be2967163ff74
ms.sourcegitcommit: c271b2edc4bf777f7194b09139ccbd174a359c75
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169020"
---
# <a name="troubleshoot-store-commerce-extension-issues"></a>Store Commerce 拡張機能の問題のトラブルシューティング

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce Store Commerce アプリの拡張機能の問題に関するトラブルシューティングの方法について説明します。

## <a name="extensions-packages-arent-loaded"></a>拡張機能パッケージが読み込まれない

### <a name="extensions-packages-dont-appear-on-the-pos--settings-page"></a>[POS] \> [設定] ページに拡張機能パッケージが表示されない

Commerce Runtime (CRT) トリガーが更新されていないため拡張機能パッケージが含まれていないか、展開されいません。 詳細については、[Commerce Runtime (CRT) の拡張性とトリガー](../dev-itpro/commerce-runtime-extensibility-trigger.md) を参照してください。

### <a name="extensions-packages-appear-on-the-pos--settings-page-but-the-manifest-isnt-loaded"></a>[POS] \> [設定] ページに拡張機能パッケージが表示されるが、マニフェストが読み込まれない

**C:\\Program Files\\Microsoft Dynamics 365\\10.0\\Store Commerce\\Extensions** フォルダーに拡張機能パッケージが存在することを確認します。 パッケージが存在する場合、マニフェストを含む **POS** フォルダーが存在します。

**POS** フォルダーがない場合、Store Commerce プロジェクトが販売時点管理 (POS) 拡張プロジェクトを正しく参照するようにします。 プロジェクトの参照パスを検証し、存在することを確認します。 

次の例の図では、インストーラー プロジェクトに、参照先の拡張プロジェクトに関する問題が発生しています。

![Store Commerce インストーラーのプロジェクト参照が無効です。](media/ReferenceNotValid.png)

拡張プロジェクトへの参照が正しく追加された場合、次の例の図ように、インストーラー プロジェクトに警告や依存関係の問題は発生しません。

![Store Commerce インストーラーのプロジェクト参照が有効です。](media/ReferenceValid.png)
