---
title: Dataverse 統合のコンフィギュレーション
description: このトピックでは、Microsoft Dataverse と Dynamics 365 Human Resources 間の統合について説明します。
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3c942358772e8ca92774decc3d4b6914fab65e22
ms.sourcegitcommit: 72a82e9aeabbdecf57e1aee72975c63eba75143a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/24/2021
ms.locfileid: "7414612"
---
# <a name="configure-dataverse-integration"></a>Dataverse 統合のコンフィギュレーション

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dataverse と Dynamics 365 Human Resources の統合を有効化また無効化にできます。 また、同期の詳細を表示し、追跡データをクリアし、テーブルを再同期して、2 つの環境間のデータ問題のトラブルシューティングに役立てることもできます。

> [!NOTE]
> Dataverse (旧 Common Data Service) および用語更新の詳細については、[Microsoft Dataverse とは何ですか?](/powerapps/maker/data-platform/data-platform-intro)を参照してください

統合をオフにすると、ユーザーは Human Resources または Dataverse に変更を加えることができますが、これらの変更は 2 つの環境間で同期されません。

既定では、Human Resources とDataverse 間の統合はオフになっています。

次のような場合は、統合を無効にすることもできます:

- Data Management Framework を介したデータに入力し正しい状態にするには、データを複数回インポートする必要があります。

- Human Resources または Dataverse のいずれかのデータに問題があります。 統合を無効にする場合、他では削除せず、もう一方の環境でレコードを削除することができます。 統合をオンに戻すと、削除されなかった環境のレコードは、削除された環境に同期します。 同期は次に、 **同期リクエストを失敗した Dataverse 統合** バッチ ジョブが実行するときに開始されます。

> [!WARNING]
> データ統合を無効する場合、両方の環境で同じレコードを編集しないようにしてください。 統合を有効に戻すと、最後に編集したレコードが同期されます。 したがって、両方の環境でレコードに同じ変更を加えていない場合は、データが失われる可能性があります。

## <a name="access-the-dataverse-integration-page"></a>Dataverse 統合のページにアクセス

1. Dataverse による統合の設定を表示または構成を希望する Human Resources インスタンスで、**システム管理** のタイルを選択します。

    [![システム管理のタイル。](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)

2. **リンク** タブを選択します。

    [![リンク タブ。](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)

3. **統合** で、**Dataverse 統合** を選択します。

    [![Dataverse コンフィギュレーション リンク。](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)

## <a name="turn-data-integration-between-human-resources-and-dataverse-on-or-off"></a>Human Resources とDataverse 間でのデータ統合を有効化また無効化

- 統合を有効にするには、**Microsoft Dataverse 統合** ページで、**Dataverse 統合を有効化する** オプションを **はい** に設定します。

    > [!NOTE]
    > 統合を有効にすると、データは次に **同期リクエストを失敗した Dataverse 統合** バッチ ジョブを実行する時に同期されます。 バッチ ジョブが完了すると、すべてのデータを使用できるようになります。

- 統合を無効にするには、オプションを **いいえ** に設定します。

[![Dataverse 統合を有効化または無効化。](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)

> [!WARNING]
> データ移行タスクの実行中は、 Dataverse 統合をオフにすることを強くお勧めします。 大規模なデータのアップロードはパフォーマンスに大きな影響を与える可能性があります。 たとえば、2000 件の作業者をアップロードすると、統合が有効になっている場合には数時間かかりますが、無効になっている場合は1時間もかかりません。 この例で示している数値は、デモンストレーションの目的でのみ使用されます。 レコードのインポートにかかる正確な時間は、さまざまな要因によって多くの影響を受けます。

## <a name="view-data-integration-details"></a>データ統合の詳細を表示

**Microsoft Dataverse 統合** ページの **管理** クイック タブで、行が Human Resources と Dataverse 間でどのようにリンクされているかを確認できます。

- テーブルの行を表示するには、**Dataverse テーブル** フィールドのテーブルを選択します。 グリッドには、選択したテーブルにリンクされているすべての行が表示されます。

> [!NOTE]
> すべての Dataverse テーブルが、現在リストにあるわけではありません。 カスタム フィールドの使用をサポートしているテーブルだけが、グリッドに表示されます。 Human Resources の継続的リリースにより、新しいテーブルが利用可能になります。

グリッドには、次のフィールドが含まれています。

- **Dataverse テーブル** – Dataverse のテーブルの名称です。
- **Dataverse エンティティ参照** – Dataverse がレコードの識別に使用する識別子です。 この値は、Human Resources **RecId** 値と同じです。 Microsoft Excel で Dataverse テーブルを開くと、識別子を確認できます。
- **Human Resources エンティティ名** – 最後にデータを Dataverse に同期させた Human Resources エンティティです。 エンティティは、Dataverse の接頭語または別の接頭語を持つことが可能です。
- **Human Resources 参照** – Human Resources のレコードに関連付けられる **Recld** 値。
- **Dataverse から削除** - Dataverse から行が削除されたかどうかを示す値です。

> [!NOTE]
> Human Resources のレコードは、Dataverse の行に対応します。

## <a name="remove-the-association-of-a-human-resources-record-from-a-dataverse-row"></a>Dataverse の行から人事レコードの関連付けを削除します

Human Resources と Dataverse 間のデータ同期中に問題が発生した場合、追跡をクリアにして追跡テーブルを再同期させることで、問題を解決できる可能性があります。 関連付けを削除してから Dataverse の行を変更または削除すると、変更内容は Human Resources に同期されません。 Human Resources で変更を加えると、新しい追跡レコードが作成され、Dataverse で行が更新されます。

- Human Resources レコードと Dataverse の行関連付けを削除するには、**Dataverse テーブル** のフィールドでテーブルを選択し、**追跡情報の削除** を選択します。

[![追跡情報をクリア。](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)

追跡を削除した後、テーブルの完全同期を実行するには、次の手順を参照してください。

## <a name="sync-a-table-between-human-resources-and-dataverse"></a>Human Resources と Dataverse 間のテーブルを同期する

この手順は、次の場合に使用します:

- Dataverse からの変更は、Human Resources に表示されるまでに時間がかかりすぎます。

- 追跡をクリアした後、追跡テーブルを最新の情報に更新する必要があります。

Human Resources と Dataverse の間のテーブルで完全同期を実行するには :

1. **Dataverse テーブル** フィールドで、テーブルを選択します。

2. **今すぐ同期** を選択します。

[![完全同期の実行。](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)

## <a name="see-also"></a>参照

[Dataverse テーブル](hr-developer-entities.md)<br>
[構成 Dataverse 仮想テーブル](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Human Resources 仮想テーブルに関するよく寄せられる質問](hr-admin-virtual-entity-faq.md)<br>
[Microsoft Dataverse とは](/powerapps/maker/data-platform/data-platform-intro)<br>
[用語の更新](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
