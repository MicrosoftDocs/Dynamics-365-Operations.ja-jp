---
title: ワークフローに関するよく寄せられる質問
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations のワークフロー システムについてよく寄せられる質問に回答します。
author: ChrisGarty
manager: AnnBe
ms.date: 05/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f6240b1b5136937aa47f455547fed6f0c7c08e2c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509294"
---
# <a name="workflow-system"></a>ワークフロー システム

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations のワークフロー システムについてよく寄せられる質問に回答します。

## <a name="notifications"></a>通知

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>作業項目が否認された場合に複数の通知が受信されるのはなぜですか。
作業項目が否認されると、その作業項目は否認済として完了します。 別の作業項目が作成され、作成者に割り当てられます。 これは、否認された作業項目に関する発信者への通知と、新しい「変更要求済」の作業項目に割り当てられたユーザーへの個別の通知があることを意味します。 

各通知は異なる作業項目に対するものですが、類似性により混乱が生じる可能性があります。 将来のリリースでこれを改善する方法を検討しています。

### <a name="why-are-my-workflow-exports-failing"></a>ワークフローのエクスポートが失敗するのはなぜですか。
現在、ワークフローのエクスポート機能には、ワークフロー名が 48 文字を超えないようにする制限があります。 48 文字を超える名前を使用すると、「サーバーは要求の認証に失敗しました」というエラーが発生するか、またはファイルがファイル タイプなしでエクスポートされるのを防ぐことができます。 詳細については、次のブログ記事を参照してください [ワークフローのエクスポートに関するトラブルシューティング](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting)。
