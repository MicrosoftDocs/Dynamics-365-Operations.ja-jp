---
title: 優先順位に基づく調整
description: このトピックでは、OData およびカスタム サービス ベース統合の優先順位に基づく調整に関する情報を提供します。
author: hasaid
ms.date: 11/18/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 21311
ms.assetid: 5ff7fd93-1bb8-4883-9cca-c8c42ddc1746
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Platform update 37
ms.openlocfilehash: ec64a37c701f87090899ee245d839b8ce115529b
ms.sourcegitcommit: 777cf334c1e3b2a867c6224aa5b43c834e8d6c27
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/19/2021
ms.locfileid: "7826549"
---
# <a name="priority-based-throttling"></a>優先順位に基づく調整

[!include [banner](../includes/banner.md)]

> [!NOTE]
> 優先順位に基づく調整は、Dynamics 365 Finance バージョン 10.0.19 から既定で有効になります。 バージョン 10.0.19 に更新する前に環境を準備する方法については [FAQ ドキュメント](throttling-faq.md) を参照してください。 この機能をテストするには、**調整優先順位マッピング** ページで統合優先順位をコンフィギュレーションします。


> [!IMPORTANT]
> [KB 4615823](https://fix.lcs.dynamics.com/Issue/Details?kb=4615823&bugId=560394&dbType=3&qc=bdc60364311159f2509ed641a0d858a46b5c57effbae2ffe778cd41f2109f7e9) には優先順位に基づく調整エクスペリエンスに直接影響する 2 つの重要な修正が含まれています。 
> 
> この修正により、環境内で調整イベントが発生した場合に 429 HTTP メッセージが送信され、そのイベントが環境に対する正しいしきい値の計算を反映するようにします。 
>
> この修正は、品質更新プログラム 10.0.17 の一部として利用できます。 このバージョンをインストールして、環境に対して優先順位に基づく調整を行う準備ができていることを確認するようお勧めします。

優先順位に基づく調整により、サービス保護設定を導入し、リソースの過剰使用率を回避してシステムの応答性を維持し、Finance and Operations アプリを実行する環境において一貫した可用性とパフォーマンスを確保できます。


優先順位に基づく調整では、ビジネスにとって重要なこれらの統合の必要性に応じて、OData とカスタム サービス ベース統合の相対的な優先順位を設定することができます。 調整マネージャーは、これらの要求に対して設定されたこれらの優先順位を受け入れます。

- OData およびカスタム サービス要求では、システムの正常性とパフォーマンスが影響を受けると、「要求過多」 を示すエラーが送信されます。 
- **Lifecycle Services (LCS) の監視** ページで調整イベントを照会できます。  

**調整優先順位マッピング** ページは、要求が調整された場合、優先順位が受け入れられるように統合の優先順位を割り当てるために使用されます。 

適切な優先順位を設定することにより、優先順位の低い統合を優先順位の高い統合の前に調整することができます。 統合の設定方法の詳細については、[外部サービスとの接続を有効にする](/learn/modules/integrate-azure-finance-operations/7-connect-external) を参照してください。 

Microsoft Azure Active Directory (Azure AD) では、次の 2 種類のアプリケーションがサポートされています。

- ユーザー ベース - このフローでは、認証と承認にユーザー名とパスワードを使用します。 
- Azure AD アプリケーション ベース - 機密クライアントとは、クライアント パスワードを機密保持できるアプリケーションのことです。 承認サーバーは、このクライアント パスワードをクライアント アプリケーションに割り当てています。 

詳細については、[認証](services-home-page.md) を参照してください。
 
## <a name="configure-priorities-for-integrations"></a>統合優先順位のコンフィギュレーション 

サービスを Azure AD および Finance and Operations アプリに登録すると、統合優先順位を設定できます。

> [!NOTE]
> 設定を完了するには、システム管理者または統合優先順位マネージャー ロールを割り当てる必要があります。 

1. Finance and Operations アプリで、 **システム管理** > **設定** > **調整優先順位マッピング** に移動します。 
2.  **新規** を選択します。 
3.  **認証タイプ** フィールドで、統合シナリオに基づいて **ユーザー** または **Azure AD アプリケーション** を選択します。
4. **Azure AD アプリケーション タイプ** を選択した場合、Azure Active Directory アプリケーションで登録したアプリケ―ションを **クライアント ID** フィールドで選択します。
5. **ユーザー タイプ** が選択されている場合は、 **ユーザー ID** フィールドで適切なサービス アカウント ユーザー ID を選択します。
6. 適切な優先順位を割り当て、**保存** を選択します。

## <a name="retry-operations"></a>再試行操作 

要求が調整されると、ユーザーからの新しい要求を処理できるようになるまでの期間を示す値がシステムによって提供されます。 要求が調整され、429 エラーが発生した場合、応答ヘッダーは **再試行** 間隔を含み、指定された秒数の経過後に要求を再試行するために使用できます。 次の例は、この操作を示しています。 

```C#
    if (!response.IsSuccessStatusCode) 
            { 
                if ((int)response.StatusCode == 429) 
                { 
                    int seconds = 30; 
                    //Try to use the Retry-After header value if it is returned. 
                    if (response.Headers.Contains("Retry-After")) 
                    { 
                        seconds = int.Parse(response.Headers.GetValues("Retry-After").FirstOrDefault()); 
                    } 
                    Thread.Sleep(TimeSpan.FromSeconds(seconds)); 



                    // Retry sending the request.
                } 
            } 
```


## <a name="monitoring"></a>監視

調整機能でオンボード エクスペリエンスを成功させるには、OData およびカスタム サービス統合パターンも監視できる必要があります。 管理センターである Microsoft Dynamics Lifecycle Services (LCS) には、管理している環境を正確に表示できることを保証する監視および診断ツールのコレクションが含まれています。 詳細については、 [Lifecycle Services (LCS) の監視および診断ツール](../lifecycle-services/monitoring-diagnostics.md)を参照してください。

一連の定義済クエリを使用して、問題の未加工ログを取得することができます。 さらに高度な分析を行うためにログをエクスポートすることができます。 以下のタイプのクエリを使用できます。

- すべての調整イベント
- 調整済みの要求

## <a name="access-the-monitoring-and-diagnostics-portal"></a>監視および診断ポータルへのアクセス

1. LCS で、適切なプロジェクトを開きます。
2. **環境** セクションで、表示する環境を選択してから **完全な詳細** を選択します。
3. **環境の詳細** ページで、**環境の監視** を選択して、監視および診断ポータルを開きます。 
4. **環境の監視** ページで、**活動** タブを選択して、**未加工ログ** ページを表示します。 
5. **クエリ名** を選択し、調整されたすべての Odata およびカスタム サービス要求の **調整済みの要求** を選択します。

> [!NOTE]
> LCS で、**すべての調整イベント** レポートは削除されました。 このレポートは、調整の対象となるサンプル要求を強調する方法として、優先順位に基づく調整が一般に利用可能になる前に導入されました。 **調整済みの要求** レポートは、調整の対象となる要求のより一貫性のあるビューを提供し、環境に関する情報を得るために使用する必要があります。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
