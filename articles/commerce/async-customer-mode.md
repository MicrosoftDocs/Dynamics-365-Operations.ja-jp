---
title: 顧客作成モードを非同期化する
description: このトピックでは、Microsoft Dynamics 365 Commerce の非同期顧客作成モードについて説明します。
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 22bb4eaf3d4897904412120fa5580c42637b56e0
ms.sourcegitcommit: eef5d9935ccd1e20e69a1d5b773956aeba4a46bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2021
ms.locfileid: "7913803"
---
# <a name="asynchronous-customer-creation-mode"></a>顧客作成モードを非同期化する

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce の非同期顧客作成モードについて説明します。

Commerce には、同期と非同期の 2 つの顧客作成モードがあります。 既定では、顧客は同期的に作成されます。 つまり、これらはリアルタイムに Commerce 本社に作成されます。 同期の顧客作成モードは、新しい顧客がチャンネルを越えてすぐに検索可能であることが利点です。 ただし、欠点もあります。 Commerce 本社への [Commerce Data Exchange: リアルタイム サービス](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service)呼び出しを生成するため、多数の顧客作成呼び出しが同時に行われると、パフォーマンスに影響を与える可能性があります。

店舗の機能プロファイルで **顧客を非同期モードで作成** オプションが **はい** に設定されている場合 (**Retail と Commerce \> チャネル設定 \> オンライン ストアの設定 \> 機能プロファイル**)、チャネル データベースに顧客レコードを作成するためにリアルタイム サービス コールは使用されません。 非同期の顧客作成モードは、Commerce 本部のパフォーマンスには影響しません。 一時的なグローバル固有識別子 (GUID) は、すべての新しい同期顧客レコードに割り当てられ、顧客 ID として使用されます。 この GUID は、販売時点管理 (POS) ユーザーには示されません。 代わりに、これらのユーザーには、顧客 ID として **同期を保留中** と表示されます。

> [!IMPORTANT]
> POS がオフラインになると、非同期顧客作成モードが無効になっている場合でも、システムは自動的に顧客を非同期で作成します。 したがって、同期顧客または非同期顧客の作成の選択にかかわらず、Commerce 本社の管理者は、**P ジョブ**、**非同期モードから顧客とビジネス パートナーを同期する** ジョブ  (旧 **非同期モードから顧客とビジネス パートナーを同期する** ジョブ)、および **1010** ジョブに対して定期的なバッチ ジョブを作成しスケジュールする必要があります。これにより、非同期顧客は Commerce 本部で同期顧客に変換されます。

## <a name="async-customer-limitations"></a>非同期顧客の制限

現在、非同期顧客機能には次の制限があります:

- 顧客が Commerce 本社で作成され、新しい顧客 ID がチャネルに同期されない限り、非同期顧客レコードを編集することはできません。
- 新しい顧客 ID をチャネルに同期しない限り、ロイヤルティ カードを非同期顧客に発行することはできません。

## <a name="async-customer-enhancements"></a>非同期顧客の強化

Commerce のバージョン 10.0.24 リリースでは、**機能管理** ワークスペースで **拡張同期顧客作成** 機能を有効にできます。 この機能は、POS と電子コマースの同期顧客作成モードの間のギャップを、次の方法で埋めます。

- 所属は非同期の顧客に関連付けることはできません。
- タイトルは、同期顧客に追加できます。
- 非同期顧客は、二次的な電子メール アドレスと電話番号を取得できません。

Commerce のバージョン 10.0.22 リリースでは、**機能管理** ワークスペースで **顧客アドレスの非同期作成を有効にする** 機能を有効にできます。 この機能により、同期顧客と非同期顧客の両方に対して、新しく作成された顧客アドレスを非同期で保存することができます。

前述した機能を有効にした後、Commerce 本部の管理者は、**P ジョブ**、**非同期モードからの顧客とビジネス パートナーの同期** ジョブ、および **1010** ジョブの定期的なバッチ ジョブを作成およびスケジュールする必要があります。これにより、すべての非同期顧客が Commerce 本社で同期顧客に変換されます。

### <a name="customer-creation-in-pos-offline-mode"></a>POS オフライン モードでの顧客作成

前述の通り、POS がオフラインになると、非同期顧客作成モードが無効になっている場合でも、システムは自動的に顧客を非同期で作成します。 したがって、Commerce 本社の管理者は、**P ジョブ**、**非同期モードからの顧客とビジネス パートナーの同期** ジョブ、および **1010** ジョブの定期的なバッチ ジョブを作成およびスケジュールする必要があります。これにより、すべての非同期顧客が Commerce 本社で同期顧客に変換されます。

> [!NOTE]
> **コマース チャネル スキーマ** ページで **共有顧客データ テーブルのフィルター** オプションが **はい** に設定されている場合 (**Retail と Commerce \> 本社の設定 \> コマース スケジューラ \> チャネル データベース グループ**)、顧客レコードは POS オフライン モードでは作成されません。 詳細については、[オフライン データの除外](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)を参照してください。

## <a name="additional-resources"></a>追加リソース

[店舗内の顧客管理](customer-mgmt-stores.md)

[非同期顧客を同期顧客に変換する](convert-async-to-sync.md)

[顧客属性](dev-itpro/customer-attributes.md)

[オフライン データの除外](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
