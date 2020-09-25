---
title: 優先順位に基づく調整
description: このトピックでは、Odata とカスタム サービス ベース統合に関する優先順位に基づく調整に関する情報を提供します。
author: hasaid
manager: AnnBe
ms.date: 07/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 21311
ms.assetid: 5ff7fd93-1bb8-4883-9cca-c8c42ddc1746
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Platform update 37
ms.openlocfilehash: 640f52d01ec41ec370f6d4cf887c72741abdd2d6
ms.sourcegitcommit: 27233e0fda61dac541c5210ca8d94ab4ba74966f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/03/2020
ms.locfileid: "3652203"
---
# <a name="priority-based-throttling"></a>優先順位に基づく調整

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

優先順位に基づく調整により、リソースの過剰使用率を回避してシステムの応答性を維持し、Dynamics 365 Finance and Operations アプリケーションを実行する環境において一貫した可用性とパフォーマンスを確保できます。

- 統合には、ビジネスで重要なニーズに基づいて優先順位を付けられます。 調整では、これらの優先順位を受け入れます。 
- OData とカスタム サービス要求では、429 エラー「要求過多」が発生します。 
- **Lifecycle Services (LCS) の監視**ページで調整イベントを照会できます。  

優先順位に基づく調整では、ビジネスにとって重要な統合の必要性に応じて、OData とカスタムのサービス ベース統合の優先順位を設定することができます。

**統合優先順位**ページでは、要求が調整された場合、優先順位が受け入れられるように統合の優先順位を割り当てます。 

適切な優先順位を設定することにより、統合に基づいて優先順位の低い統合を、優先順位の高い統合の前に調整することができます。 統合の設定方法の詳細については、[外部サービスとの接続を有効にする](https://docs.microsoft.com/learn/modules/integrate-azure-finance-operations/7-connect-external) を参照してください。 

Microsoft Azure Active Directory (Azure AD) では、次の 2 種類のアプリケーションがサポートされています。

- ユーザー ベース - このフローでは、認証と承認にユーザー名とパスワードを使用します。 
- Azure AD アプリケーション ベース - 機密クライアントとは、クライアント パスワードを機密保持できるアプリケーションのことです。 承認サーバーは、このクライアント パスワードをクライアント アプリケーションに割り当てています。 

詳細については、[認証](services-home-page.md) を参照してください。
 
## <a name="configure-priorities-for-integrations"></a>統合優先順位のコンフィギュレーション 

サービスを Azure AD および Finance and Operations アプリに登録すると、統合優先順位を設定できます。

> [!NOTE]
> 設定を完了するには、システム管理者または統合優先順位マネージャー ロールを割り当てる必要があります。 

1. Finance and Operations アプリで、 **システム管理** > **設定** > **調整優先順位マッピング**に移動します。 
2.  **新規**を選択します。 
3.  **認証タイプ** フィールドで、統合シナリオに基づいて**ユーザー**または **Azure AD アプリケーション**を選択します。
4. **Azure AD アプリケーション タイプ**を選択した場合、Azure Active Directory アプリケーションで登録したアプリケ―ションを **クライアント ID** フィールドで選択します。
5. **ユーザー タイプ**が選択されている場合は、 **ユーザー ID** フィールドで適切なサービス アカウント ユーザー ID を選択します。
6. 適切な優先順位を割り当て、**保存**を選択します。

## <a name="retry-operations"></a>再試行操作 

要求が調整されると、ユーザーからの新しい要求を処理できるようになるまでの期間を示す値がシステムによって提供されます。 要求が調整され、429 エラーが発生した場合、応答ヘッダーは **再試行**間隔を含み、指定された秒数の経過後に要求を再試行するために使用できます。 次の例は、この操作を示しています。 

```x++
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