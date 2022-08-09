---
title: スロットリング優先度
description: この記事では、OData およびカスタム サービス ベース統合の優先順位に基づく調整に関する情報を提供します。
author: jaredha
ms.date: 05/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 21311
ms.assetid: 5ff7fd93-1bb8-4883-9cca-c8c42ddc1746
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Platform update 37
ms.openlocfilehash: 95581f7c5b43b81c7c7497d64430a5a8736c275b
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2022
ms.locfileid: "9108515"
---
# <a name="throttling-prioritization"></a>スロットリング優先度

[!include [banner](../includes/banner.md)]

この記事では、Open Data Protocol (OData) をカスタム サービス ベース統合の優先順位に基づく調整に関する情報を提供します。

サービス保護アプリケーション プログラミング インターフェイス (API) のリソース ベースの制限は、サービス保護 API のユーザー ベースの制限と連携し、リソースの過剰利用を防ぐのに役立つ保護設定として機能します。 これにより、システムの応答性を維持し、財務と運用アプリを実行する環境で一貫した可用性とパフォーマンスを実現できます。 リソース ベースの制限は、Web サーバー リソースの総消費量がサービスのパフォーマンスと可用性を低下させるレベルに達すると、サービス要求を調整します。

リソース ベースのサービス保護 API の制限では、ビジネスにとって重要なこれらの統合の必要性に応じて、OData とカスタム サービス ベース統合の相対的な優先順位を設定することができます。 調整マネージャーは、要求に対して設定されたその優先順位を受け入れます。 OData およびカスタム サービス ベース要求では、システムの正常性とパフォーマンスが影響を受けると、「要求過多」 のエラーが送信されます。

**調整優先順位マッピング** ページは、要求が調整された場合、優先順位が受け入れられるように統合の優先順位を割り当てるために使用されます。 

適切な優先順位を設定することにより、優先順位の低い統合を優先順位の高い統合の前に調整することができます。 統合の設定方法の詳細については、[外部サービスとの接続を有効にする](/learn/modules/integrate-azure-finance-operations/7-connect-external) を参照してください。 

Azure Active Directory (Azure AD) では、次の 2 種類のアプリケーションがサポートされています:

- **ユーザー ベース** – このフローでは、認証と承認にユーザー名とパスワードを使用します。 
- **Azure AD アプリ ベース** – 機密クライアントとは、クライアント パスワードを機密保持できるアプリケーションのことです。 承認サーバーは、このクライアント パスワードをクライアント アプリケーションに割り当てています。 

詳細については、[認証](services-home-page.md) を参照してください。
 
## <a name="configure-priorities-for-integrations"></a>統合優先順位のコンフィギュレーション 

サービスを Azure AD および財務と運用アプリに登録すると、統合優先順位を設定できます。

> [!NOTE]
> 設定を完了するには、**システム管理者** または **統合優先順位マネージャー** ロールを割り当てる必要があります。 

1. 財務と運用アプリで、 **システム管理** > **設定** > **調整優先順位マッピング** の順に移動します。 
2.  **新規** を選択します。 
3.  **認証タイプ** フィールドで、統合シナリオに基づいて **ユーザー** または **Azure AD アプリケーション** を選択します。
4. **Azure AD アプリケーション タイプ** を選択した場合、Azure Active Directory アプリケーションで登録したアプリケ―ションを **クライアント ID** フィールドで選択します。
5. **ユーザー タイプ** が選択されている場合は、 **ユーザー ID** フィールドで適切なサービス アカウント ユーザー ID を選択します。
6. 適切な優先順位を割り当て、**保存** を選択します。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

