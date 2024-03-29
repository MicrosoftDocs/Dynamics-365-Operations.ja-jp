---
title: 小売店舗での財務調整
description: この記事では、Microsoft Dynamics 365 Commerce の POS 用小売店舗での財務調整について説明します。
author: anpurush
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-21
ms.dyn365.ops.version: ''
ms.openlocfilehash: 19c0f6edd7756a611a234a162418ef5826bd5cc2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860247"
---
# <a name="financial-reconciliation-in-retail-stores"></a>小売店舗での財務調整

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Commerce バージョン 10.0.10 以前では、販売時点管理 (POS) クライアントが販売店の月末プロセスに対して提供する機能により、店員と店舗の管理者は日常業務を行うことができます。 たとえば、支払/入金申告、ブラインド クローズのシフト、シフト トランザクションの調整、およびシフトの決算を行うことができます。 ただし、POS にはシフトの財務情報を最終的に転記するために使用できる機能はないので、Commerce 本社で財務を転記するために使用できます。 通常、店舗管理者はこのタスクを完了する責任があります。 シフトでサイン オフするには、情報を確認して必要に応じて修正を行い、そのシフトの合計を確定する必要があります。 最終的な合計は、Commerce 本社の財務モジュールに転記する必要があります。

さらに、Commerce バージョン 10.0.10 では、店舗管理者が Commerce 本社の明細行を確認し、調整できます。 ただし、機能は制限されており、店舗の管理者が Commerce 本社のクライアントにアクセスすることはほとんどありません。 さらに、財務上の明細書レビューおよび調整は、明細書が Commerce 本社で作成されている場合にのみ実行できます。 ただし、プロセスは通常、毎晩実行されます。 したがって、店舗管理者は、財務小売明細書が Commerce 本社で作成されるとき、シフトのサイン オフが終了するまで待機する必要があります。

Commerce バージョン 10.0.11 以降において、店舗管理者は POS クライアント自体でのシフト確認、調整、および完了を行うことができます。 その後、そのデータを使用して、Commerce 本社で財務小売明細書を作成および転記することができます。

> [!NOTE]
> 小売店舗での財務調整に関連する機能は、トリクル フィードベース注文の作成が有効になっている場合にのみ機能します。 詳細については、[小売店舗トランザクション用トリクル フィードベース注文の作成](trickle-feed.md) を参照してください。

## <a name="set-up-financial-reconciliation"></a>財務調整の設定

財務調整機能を使用するには、次の手順に従います。

1. **機能管理** ワークスペースで、**小売明細書 - トリクル フィード** 機能を有効にします。
1. 適切な店舗の POS 機能プロファイルで、**店舗の財務調整を有効にする** オプションを **はい** に設定します。

## <a name="more-information-about-financial-reconciliation"></a>財務調整についての詳細情報

財務調整機能を有効にすると、Commerce 本社の **小売店舗** ページの **明細書/決算** クイックタブで定義されているパラメータの一部がチャンネル データベースに同期されます。 小売明細書で使用される計算基準と金額しきい値の同じセットが適用されます。

**シフトのクローズ** 操作が呼び出されると、システムはそのシステム計算額と申告額が一致することを検証します。 違いが発見され、その違いが定義されたしきい値を超えた場合、ユーザーは必要な調整を行うよう促され、可能となります。

各支払/入金に対して調整を行うことができます。 支払/入金を選択すると、ユーザーは異なるトランザクション タイプの合計を表示したり、特定のトランザクション タイプの合計を編集したりすることができます。 編集中、システムは元の計算金額と、そのトランザクション タイプの無効金額を表示します。 ユーザーは、編集プロセスの一部としてメモをキャプチャすることもできます。 メモは監査目的で使用できます。

ユーザーは、検証プロンプトとメッセージを無視して、シフトを閉じることができます。 ただし、ユーザーが検証プロンプトを無視した場合は、同じ問題が発生し、シフトが Commerce 本社の財務諸表を転記する際に修正する必要があります。

また、POS の **シフトのクローズ** 操作は、オフライン データベース内のすべてのトランザクションがチャンネル データベースに同期されていることを検証します。 トランザクションが同期されていない場合、この状況が発生するとシステム金額が誤って計算される可能性があるため、ユーザーは警告メッセージを受け取ります。 この場合、ユーザーは **シフトのクローズ** 操作を終了して、オフライン トランザクションをチャンネル データベースに同期することができます。 別の方法として、ユーザーは同期されていないトランザクションを考慮してシステム計算額を手動で調整し、正しい財務番号のセットを確定して転記されるように行うことができます。 

トリクル フィードのステートメント転記を使用する場合、トランザクションの転記は財務の転記から切り離されるので、不足しているオフライン トランザクションのシステム計算額を調整することができます。 このようにして、欠落しているトランザクションに関係なく、財務が常に正確に計算され転記されていることを確認できます。 オフライン トランザクションは、チャンネル データベースと Commerce 本社に同期した後、財務ポスティングとは別に転記できます。

シフトの財務調整の詳細は、P- ジョブを使用して Commerce 本社に同期されます。

Commerce 本社の財務小売明細書では、合計を計算して明細行の詳細を表示することはできません。 代わりに、POS クライアントの確定額を使用して、財務小売明細書を作成および転記します。


[!INCLUDE[footer-include](../includes/footer-banner.md)]