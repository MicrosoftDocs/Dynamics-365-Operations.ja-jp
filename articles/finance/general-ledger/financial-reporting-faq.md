---
title: 財務諸表に関するよく寄せられる質問
description: このトピックでは、よく寄せられる財務諸表に関するいくつかの質問に対する回答を提供します。
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e1b67f86446403933005008a9a1e2cc6739dc516
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266636"
---
# <a name="financial-reporting-faq"></a>財務諸表に関するよく寄せられる質問

このトピックでは、よく寄せられる財務諸表に関する質問に対する回答を提供します。

## <a name="how-do-i-restrict-access-to-a-report-by-using-tree-security"></a>ツリー セキュリティを使用して、レポートへのアクセスを制限するにはどうすればよいですか。

次の例は、ツリー セキュリティを使用してレポートへのアクセスを制限する方法を示しています。

USMF デモ会社には、財務諸表のすべてのユーザーがアクセスすべきではない **貸借対照表** レポートがあります。 ツリー セキュリティを使用すると、あるレポートへのアクセスを制限して、特定のユーザーのみがそれにアクセスできるようにすることができます。

1. Financial Reporter Report Designer にサインインします。
2. **ファイル \> 新規 \> ツリー定義** の順に選択して新しいツリー定義を作成します。
3. **ユニットのセキュリティ** 列の **集計** 行をダブルタップ (またはダブルクリック) します。
4. **ユーザーとグループ** を選択します。
5. レポートにアクセスする必要があるユーザーまたはグループを選択します。
6. **保存** を選択します。
7. レポート定義で、新しいツリー定義を追加します。
8. ツリー定義で、**設定** を選択します。 **レポート ユニットの選択** で、**すべてのユニットを含む** を選択します。

## <a name="how-do-i-identify-which-accounts-dont-match-my-balances"></a>残高と一致しない勘定は、どのように識別できますか。

残高が一致しないレポートがある場合は、以下の手順に従って、各勘定と差異を特定します。

### <a name="in-financial-reporter-report-designer"></a>Financial Reporter Report Designer 内

1. 新しい行定義を作成します。
2. **編集 \> 分析コードからの行の挿入** を選択します。
3. **MainAccount** を選択します。
4. **OK** を選択します。
5. 行定義を保存します。
6. 新しい列定義を作成します。
7. 新しいレポート定義を作成します。
8. **設定** を選択し、このオプションのマークを解除します。
9. レポートを生成します。 
10. レポートを Microsoft Excel にエクスポートします。

### <a name="in-dynamics-365-finance"></a>Dynamics 365 Finance 内

1. **一般会計 \> 照会およびレポート \> 試算表** の順に進みます。
2. 次のフィールドを設定します。

    - **開始日** – 会計年度の開始日を入力します。
    - **終了日** – レポートを生成する日を入力します。
    - **財務分析コード** – このフィールドを **主勘定セット** に設定します。

3. **計算** を選択します。
4. レポートを Excel にエクスポートします。

これで、Financial Reporter Excel レポートから **試算表** レポートにデータをコピーして、**決算残高** 列を比較できます。

## <a name="when-i-design-a-report-in-report-designer-or-when-i-generate-a-financial-report-i-received-the-following-message-the-operation-could-not-be-completed-due-to-a-problem-in-the-data-provider-framework-how-should-i-respond"></a>Report Designer でレポートを設計したり、財務諸表を生成する場合に、「データ プロバイダー フレームワークの問題が原因で操作を完了できません」というメッセージが表示されます。 対応方法を教えてください。

このメッセージは、財務諸表の使用中にシステムがデータ マートから財務メタデータを取得しようとしたときに問題が発生したことを示します。 この問題に対応するには、次の 2 つの方法があります。

- Report Designer の **ツール \> 統合の状態** に移動して、データの統合の状態を確認します。 統合が不完全な場合は、完了するまで待ちます。 その後、メッセージを受信したときに行っていた操作を再試行します。
- サポートに問い合わせ、問題を特定して作業してください。 システムにデータの不整合がある可能性があります。 サポート エンジニアは、サーバー上の問題を特定し、更新が必要な可能性がある特定のデータを探す支援を行うことができます。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
