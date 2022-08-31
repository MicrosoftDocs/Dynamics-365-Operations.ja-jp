---
title: Dynamics 365 財務と運用、Enterprise edition プラットフォーム更新プログラム 11 新機能および変更された機能 (2017 年 10 月)
description: この記事では、Dynamics 365 財務と運用、Enterprise edition プラットフォーム更新プログラム 11 の新機能または変更された機能について説明します。 このバージョンは 2017 年 10 月にリリースされました。
author: sericks007
ms.date: 10/09/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2017-09-30
ms.dyn365.ops.version: Platform update 11
ms.custom: ''
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: f0401d0d764ccb5aa81d4594781360ff2a28c2a6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267184"
---
# <a name="whats-new-or-changed-in-dynamics-365-finance-and-operations-enterprise-edition-platform-update-11-october-2017"></a>Dynamics 365 財務と運用、Enterprise edition プラットフォーム更新プログラム 11 新機能および変更された機能 (2017 年 10 月)

[!include [banner](../includes/banner.md)]

この記事では、Dynamics 365 財務と運用、Enterprise edition プラットフォーム更新プログラム 11 の新機能または変更された機能について説明します。 このバージョンは 2017 年 10 月にリリースされ、ビルド番号は 7.0.4679.35176 です。

新機能についての補足情報の検索および開発中の新機能に関する詳細については、[Dynamics 365 ロードマップ](https://roadmap.dynamics.com/) を参照してください。 プラットフォーム更新プログラム 11 に含まれるバグ修正の詳細については、Lifecycle Services (LCS) にログインし、この [サポート技術情報記事](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4047244&bugId=3869536&qc=310ad7de90642ce961cc3f51358f3b40788c975dec466891d0fcc17c13145f56) を参照してください。

## <a name="attachment-presence-and-document-count-indicator"></a>添付ファイルのプレゼンスとドキュメント数のインジケータ

レコードを表示するとき、システムは、添付ファイル ボタンに数を表示することによって、そのレコードの添付ファイルの数を示します。 この数は、添付ファイルの詳細フォームに移動せずに、レコードに関連付けられた添付ファイルがあることを示します。 カウントには 9 つまでの添付ファイルが表示され、9 以上の添付ファイルが「9+」として表示されます。 詳細については、[ドキュメント管理のコンフィギュレーション](../organization-administration/configure-document-management.md) を参照してください。

## <a name="auditing"></a>監査

ユーザーのログインとサインアウトの監査が Finance and Operations で有効になりました。 ユーザーがアプリケーションにサインインまたはサインアウトすると、システムログが記録されます。 ユーザーのセッションが期限切れまたは終了する場合でも、サインアウトが記録されます。

システム管理者またはセキュリティー管理者は、**ユーザー ログ** ページ (**システム管理** \> **照会** \> **ユーザー ログ**) に移動して監査ログにアクセスできます。

## <a name="bring-your-own-database-byod-support-for-delete-operations"></a>削除操作のための自分のデータベースの持ち込み (BYOD) のサポート

自分のデータの持ち込みストア (BYOD) は、顧客が既存のデータ ウェアハウスと Finance and Operations のデータを統合するために使用する機能です。 BYOD を使用するとデータを顧客の SQL Azure データベースに段階的にエクスポートできます。 差分エクスポート フィーチャーは変更の反映に理想的ですが、一般的に初期データの設定に使用される完全なエクスポートもサポートしています。 増分操作は、出力先のデータベースへの挿入および更新操作に反映されます。 この追加機能では、ソース内の対応するレコードが削除された場合、BYOD 差分更新操作により出力先データベース内のレコードが削除されます。

## <a name="cloud-and-edge-elements"></a>クラウドおよびと Edge の要素

テーブル、ビュー、データ エンティティ、メニュー項目、およびサービス操作には、**運用ドメイン** および **サブスクライバー アクセス レベル** というメタデータ プロパティが追加されています。 [クラウドおよびエッジの配置](https://community.dynamics.com/b/msftdynamicsblog/archive/2017/02/23/the-right-cloud-option-for-your-business)をサポートするには新しいメタデータ プロパティが必要で、Microsoft Visual Studio で表示されます。

また、同じで目的で **配置**、**DeploymentAccessibleCompany**、**NumberSequenceDeployments** の 3 つのテーブルが追加されました。

現時点では、新しいプロパティとテーブルを取得する必要はありません。

## <a name="copy-legal-entity-configurations-to-a-new-legal-entity"></a>法人のコンフィギュレーションを新しい法人にコピーする

新しい会社が必要になると、ユーザーは既存の法人組織の設定を新しい会社にコピーすることで、時間を節約し、潜在的なエラーを削減することができます。 これにより、新しい場所でのオンボードが迅速になり、企業のゴールデン テンプレート デザインとの一貫性を保つことができます。

## <a name="development-and-customization---field-groups---extension-of-another-extension"></a>開発およびカスタマイズ - フィールド グループ - 他の拡張の拡張機能

TableExtension1 と TableExtension2 の 2 つのモデルに 2 つの拡張機能を持つテーブル (Table1) があるとします。 TableExtension1 には、新しいフィールド グループ (NewFieldGroup1) が含まれています。 TableExtension2 を使用すると、NewFieldGroup1 にフィールドを追加できますようになります。 フォーム拡張子に NewFieldGroup1 を追加する場合は、実行時にユーザー インターフェイスですべてのフィールドが認識され、レンダリングされます。 この機能は、Platform update 11 以前には利用できませんでした。

## <a name="development-and-customization---support-for-display-and-edit-methods-in-class-extensions"></a>開発およびカスタマイズ - クラス拡張の表示と編集メソッドのサポート

クラスの拡張機能 (テーブル クラスの拡張機能) を使用して表示を定義しメソッドを編集することができるようになりました。 次の例は、これを示しています。

LedgerJournalTransAccrual テーブルの拡張機能作成し、**MyStringField1** という名前の新しい文字列フィールドをテーブルに追加します。 テーブル クラス LedgerJournalTransAccrual を次のように拡張します。

```
[ExtensionOf(tableStr(LedgerJournalTransAccrual))]
final class MyLedgerJournalTransAccrual_Extension
{
    [SysClientCacheDataMethodAttribute(true)]
    public static display LedgerJournalAccountName
    MyLedgerAccountName(LedgerJournalTransAccrual \_ledgerJournalTransAccrual)
    {
        return \_ledgerJournalTransAccrual.MyStringField1 + "Hello";
    }
}
```

新しいフィールド グループを **MyLedgerAccountName** のテーブル拡張機能に追加し、フィールド グループの表示データ フィールドとしてメソッド **MyLedgerAccountName** を選択します。 

1. 新しいフィールド グループを追加します。
2. フィールドグループに新しいフィールドを追加します。
3. **データ フィールド** プロパティを **LedgerJournalTransAccrual\_Extension::MyLedgerAccountName** に設定します。 (それを入力するか、**データ フィールド** ドロップダウン リストから選択することができます)。

## <a name="development-and-customization---support-for-field-arrays-in-table-extensions"></a>開発およびカスタマイズ - テーブル拡張のフィールド配列のサポート

テーブルを拡張し、テーブル拡張部に新しいフィールドを追加するとき、新しいフィールドが配列の EDT タイプの場合、X++ コードから EDT 配列フィールドにアクセスできるようになります。 これを実行する方法の例を次に示します。

1. テーブル拡張子を作成します。
2. テーブル拡張機能に新しいフィールドを追加します。
3. 配列である EDT にフィールドのタイプを設定します。
4. X++ では新しい拡張子フィールドを次のように使用します。

```
A table1;
table1.EDTArrayField1[1] = 'text1';
table1.EDTArrayField1[2] = 'text2';
table1.EDTArrayField1[3] = 'text3';
// perform insert or update operations here on table 1
```

## <a name="development-and-customization---use-edt-extensions-to-customize-number-of-decimals"></a>開発およびカスタマイズ - EDT 拡張機能を使用して小数点以下桁数をカスタマイズする

EDTReal 型の拡張データ型の拡張機能を使用するとき、小数点精度の変更を確認できます。 展開している EDT 要素が持っている **番号の小数点以下が拡張可能な** プロパティが true に設定されている場合、この EDT の拡張機能を作成でき、**小数点以下なし** プロパティを変更することができます。 これにより、開発者はタイプ EDTReal の EDT の小数点精度をカスタマイズできます。 現在のプラットフォーム更新プログラム 11 では、次の EDT で小数点の拡張が可能です。量および AmountMST。

## <a name="multiple-document-reports-sent-as-a-zip-file-to-streamline-delivery"></a>配送を簡素化するために .zip ファイルとして送信する複数のドキュメント レポート

このフレームワークは、レポート セッションがダウンロード用の複数の文書を生成するシナリオをよりよく扱うように拡張されました。 セキュリティ上の事前措置として、Dynamics 365 財務と運用サービスは複数のファイルをブラウザにダウンロードするシナリオの処理方法を調整しました。 複数のドキュメントを次々と受信するのではなく、ドキュメントは 1 つの .zip ファイルにパッケージ化してダウンロードされます。 これは、顧客取引明細書や督促状などの複数のドキュメントを生成する既存のレポートに影響します。

## <a name="resource-governor-manages-server-workloads"></a>リソース ガバナーは、サーバー ワークロードを管理します。

リソース ガバナーは、システム管理者の管理オーバーヘッドを削減するコンポーネントです。 Finance and Operations にはバッチおよび処理タスクが含まれ、高速計算処理能力があります。 複数の転記ジョブがある月末のワークロードなど、業務の必要性に応じて多くのジョブをスケジュールできます。 これらの計算処理はサーバーを占有しますが、フロント オフィス プロセスなどの対話型オペレーションは、パフォーマンスの低下なしに実行することができます。

リソース ガバナーは、SQL Azure データベースから提供される組み込みのリソース ガバナンス サービスを使用します。 Dynamics 365 財務と運用ランタイム サービスでは、突然の計算スパイクがある場合、SQL Azure データベースは低下しないように対話型プロセスとバッチ プロセス (ほとんどの計算が実行される場所) の両方に売上予算を割り当てます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
