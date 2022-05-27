---
title: Dataverse 同期のリセット
description: このトピックでは、Microsoft Dynamics 365 Human Resources と Microsoft Dataverse のヒューマン キャピタル マネージメント (HCM) の共通のソリューションとの間でレコードが正しく同期されない場合のトラブルシューティングについて説明します。
author: jaredha
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-09-27
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: 8bfcd51b023c02590919155abbb836326408d298
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2022
ms.locfileid: "8696238"
---
# <a name="reset-dataverse-synchronization"></a>Dataverse 同期のリセット


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a>問題

Microsoft Dynamics 365 Human Resources  と Microsoft Dataverse のヒューマン キャピタル マネージメント (HCM) の共通のソリューションのエンティティ間でレコードが同期されない。 同期の詳細については、[Dataverse 統合の構成](hr-admin-integration-common-data-service.md)を参照してください。 **Dataverse 統合の再試行**、または **Dataverse 統合のミス リクエスト** の同期バッチジョブが **実行中** 状態で止まっていると、正しく同期ができない場合があります。

## <a name="resolution"></a>解決策

**Dataverse 統合再試行** または **Dataverse 統合未完了リクエスト同期** のバッチジョブが **実行中**、または **キャンセル中** の状態で止まっている場合、状態をリセットすることができます。 これを実行するには、[スタックしたバッチ ジョブのリセット](hr-admin-troubleshooting-batch-execution.md)に記載のガイダンスに従って、バッチジョブをキャンセルします。 キャンセルした後は、バッチ ジョブを **待機中** 状態に設定してリセットできます。 その後、次の実行予定時刻にバッチ ジョブが実行されます。

1. まだ実行していない場合は、 **機能管理** で **高度なバッチの中止** 機能を有効にします。
   1. **機能管理** ページ (**システム管理** > **集計** > **機能管理**) に移動します。
   2. **すべて** タブを選択します。
   3. **機能名** 列を選択し、**高度なバッチの中止** でフィルター処理します。
   4. まだ有効になっていない場合は、 **有効にする** アクションを選択します。

2. Dataverse 統合をオフにします。
   1. **Microsoft Dataverse 統合** ページ (**システム管理** で、**リンク** > **統合** > **Dataverse 構成**) にアクセスします。
   2. **Dataverse 統合の有効化** を **いいえ** に設定します。

3. **Dataverse 統合再試行** バッチ ジョブをキャンセルします。
   1. **バッチ ジョブ** ページ (**システム管理** で、**リンク** > **バッチ ジョブ** > **バッチ ジョブ**) にアクセスします。
   2. **職務明細書** 列を **統合** でフィルター処理します。
   3. **Dataverse 統合の再試行** バッチ ジョブを選択します。
   4. アクション リボンで、**バッチ ジョブ**、**強制キャンセル** を選択し、**はい** を選択して確認します。

   > [!NOTE]
   > 統合が初めて有効化されたタイミングによっては、バッチジョブに **Common Data Service 統合の再試行** という説明がある場合があります。 **Dataverse 統合の再試行** バッチ ジョブではなく、このバッチ ジョブ一覧表示される場合は、これを選択します。

4. すべての Dataverse 統合バッチ ジョブを削除します。
   1. **バッチ ジョブ**  ページで、**Dataverse 統合が失敗した要求の同期**、**Dataverse 統合の再試行**、**Dataverse 統合の初回同期** バッチ ジョブを選択します。
   2. アクション リボンで、**状態の変更** アクションを選択します。 
   3. **保留** を選び、**OK** を選択します。
   4. アクション リボンで、 **削除** アクションを選択し、**はい** を選択してアクションを確認します。

5. Dataverse 統合バッチ ジョブを有効にします。
   1. **Microsoft Dataverse 統合** ページ (**システム管理** > **リンク** > **統合** > **Dataverse 構成**) にアクセスします。
   2. **Dataverse 統合の有効化** を **はい** に設定します。

6. **バッチ ジョブ** ページに移動し、**Dataverse 統合の再試行** と **Dataverse i統合の失敗した要求同期** バッチ ジョブが作成されたことを確認します。

バッチ ジョブを再作成した状態で、**Dataverse 統合再試行** バッチ ジョブを監視して、ジョブの実行期間を確認できます。 その後、Microsoft Dataverse の HCM 共通ソリューションにレコードが正しく同期されていることを確認します。

## <a name="see-also"></a>参照

[Dataverse 統合のコンフィギュレーション](hr-admin-integration-common-data-service.md)<br>
[行き詰まったバッチ ジョブのリセット](hr-admin-troubleshooting-batch-execution.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
