---
title: 一般会計への補助元帳の転送
description: このトピックでは、一般会計の補助元帳の転送プロセスに関する Microsoft Dynamics 365 Finance での機能について説明します。
author: roschlom
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: d43b96176c51d12c35383da75bf65a1ad92f84c6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815287"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>一般会計への補助元帳の転送

[!include [banner](../includes/banner.md)]

このトピックでは、補助元帳仕訳のバッチの転送のルールに関連する、Microsoft Dynamics 365 Finance での機能について説明します。

バージョン 8.1 では、ルールの転送を許可するよう変更が加えられ、**同期** オプションは非推奨になりました。 詳細については、[Finance and Operations の削除済みまたは非推奨の機能](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20) を参照してください。

次のオプションは、補助元帳バッチの転送に使用できます。 

 - 非同期 – このオプションでは、総勘定元帳への補助元帳勘定項目の転送が直ちにスケジュールされます。 総勘定元帳伝票は、リソースがサーバー上でこの要求を自由に処理できるようになるとすぐに記録されます。 

- スケジュール済バッチ – このオプションでは、総勘定元帳の処理キューに転送されている補助元帳勘定項目が追加されますが、この項目は、注文を受けた順序で処理されます。 リソースがサーバー上でこのバッチ ジョブを自由に処理できる場合、総勘定元帳伝票は予定時刻に記録されます。 
 
バージョン 10.0.8 では、非同期オプションのパフォーマンスを向上させるための改良が加えられました。 この機能は、機能名 **総勘定元帳への補助元帳の転送パフォーマンスの最適化** で有効にできます。 
 
この機能により、補助元帳から総勘定元帳へのデータの転送が改善されます。 これにより、処理をより効率的にすることができ、転送する一連の小さなトランザクションをグループ化できます。 これにより、バッチ サーバーの使用がより効率的になります。 この機能には、バッチ サーバーの設定、オンライン、および非同期転送オプションが作動する機能が必要です。 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]