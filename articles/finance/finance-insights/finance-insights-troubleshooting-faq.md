---
title: Finance Insights の設定に関する問題のトラブルシューティング
description: このトピックでは、Finance insights の機能の使用時に発生する問題を一覧表示します。 また、これらの問題の修正方法についても説明します。
author: panolte
ms.date: 08/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-20
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 7ff42ffc334147c1a4c6b6349c86580df7f1955b
ms.sourcegitcommit: 47a3ad71210c7ac84d0c25e913c440b5ba205282
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/23/2021
ms.locfileid: "7512893"
---
# <a name="troubleshoot-finance-insights-setup-issues"></a>Finance Insights の設定に関する問題のトラブルシューティング

[!include [banner](../includes/banner.md)]

このトピックでは、Finance insights の機能の使用時に発生する問題を一覧表示します。 また、これらの問題の修正方法についても説明します。

## <a name="symptom-why-cant-i-map-the-customer-payment-insights-data-integration-template-destination-column"></a>現象: 顧客支払情報データ統合テンプレートの宛先列をマッピングできないのはなぜですか？

### <a name="resolution"></a>解決策

以前のバージョンのテンプレートを使用している可能性があります。 バージョン 10.0.17 のリリース前に、**顧客が支払予測結果 (プレビュー)** エンティティを使用して **顧客支払情報の結果 (CDS to Fin and Ops)** データ統合 (DI) テンプレートを構成してプレビューを表示しました。 10.0.17 以降にアップグレードした後、**顧客支払情報の結果 (CDS to Fin and Ops 10.0.17 以降)** を使用してマッピングを完了する必要があります。 データ管理エンティティの一覧が更新され、 **支払予測結果** エンティティが表示されるまでは、DI テンプレートの宛先列をマッピングできない場合があります。 エンティティ リストを更新し、支払い予測結果を表示するには、Microsoft Dynamics 365 Finance と Dataverse (旧名: Common Data Service \[CDS\] 管理者ポータル) の両方の手順を完了します。

### <a name="in-finance"></a>Finance

アップグレード後は、Finance に関する次の手順に従います。

1. **システム管理 \> ワークスペース \> データ管理** の順に移動します。
2. **データ管理** ワークスペースで、**フレームワーク パラメーター** タイルを選択します。
3. **データのインポート/エクスポート フレームワークのパラメータ** ページで、**エンティティ設定** を選択し、**エンティティの一覧の更新** を選択します 。
4. **データのインポート/エクスポート フレームワークのパラメーター** ページを閉じます。
5. **データ管理** ワークスペースで、**フレームワーク パラメーター** タイルを選択します。
6. "支払予測の結果" を検索します。 **支払予測結果** エンティティがプレビュー バージョンから削除されたことを確認します。 プレビュー バージョンの場合、名前の最後は "(プレビュー)" となっています。 エンティティのプレビュー バージョンのみ表示される場合は、Microsoft サポートに問い合わせください。

### <a name="in-dataverse"></a>Dataverse 内

[Power Platform管理センター](https://admin.powerplatform.microsoft.com/environments)で次の手順 に従って、データ統合プロジェクトを更新します。

1. Finance insights のプレビュー版を使用している場合は、**顧客支払情報の結果 (CDS to Fin and Ops)** テンプレートに関連付けられている DI プロジェクトを削除します。
2. [データ インテグレータ プロジェクトの作成](create-data-integrate-project.md)の手順に従います。 **顧客支払情報の結果  (CDS to Fin and Ops 10.0.17 以降)** テンプレートを使用します。

## <a name="symptom-why-doesnt-the-cash-forecast-tab-in-the-cash-flow-forecast-workspace-show-any-data"></a>現象: キャッシュ フロー予測ワークスペースの「キャッシュの予測」タブにデータが表示されないのはなぜですか？

### <a name="resolution"></a>解決策

**キャッシュ フローの予測** ワークスペースにデータを正しく表示するには、「現金と銀行管理」のキャッシュ フロー予測機能と Finance insights のキャッシュ フロー予測機能が設定され、有効化されている必要があります。

最初に、キャッシュ フロー予測口座と流動性口座を設定し、有効にします。 詳細については、「[キャッシュ フロー予測](../cash-bank-management/cash-flow-forecasting.md)」を参照してください。 この設定が完了したにもかかわらず、期待通りの結果が得られない場合は、[キャッシュ フロー予測の設定のトラブルシューティング](../cash-bank-management/cash-flow-forecasting-tsg.md)を参照してください。

次に、Finance insights のキャッシュ フロー予測機能 (**現金と銀行管理 \> 設定 \> Finance Insights \> キャッシュ フロー予測**) が有効になっていること、AI モデルの学習が完了していることを確認します。 トレーニングが完了しない場合は、**今すぐ予測** を選択してモデルのトレーニング プロセスを開始します。
