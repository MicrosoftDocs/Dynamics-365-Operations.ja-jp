---
title: AX 2012 からのアップグレード - Go live (切替)
description: このトピックでは、コードとデータベースのアップグレード バージョンの実行している Dynamics AX 2012 から Finance and Operations アプリの最終的な切替えプロセスについて説明します。
author: jorisdg
ms.date: 08/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2018-03-31
ms.dyn365.ops.version: Platform update 12
ms.openlocfilehash: 21f7da26a911417ba6f67e471050e25862b3a3ad
ms.sourcegitcommit: 696796ca5635863850ae9ef16fc1fb0fc46ce8f0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/28/2021
ms.locfileid: "7441329"
---
# <a name="upgrade-from-ax-2012---go-live-cutover"></a>AX 2012 からのアップグレード - Go live (切替)

[!include [banner](../includes/banner.md)]

[!include [upgrade banner](../includes/upgrade-banner.md)]

標準またはプレミア承認テスト環境 (サンドボックス レベル 2 またはそれ以上) でアップグレード テストを正常に完了し、正常にテスト切替を完了した後が、実稼働環境をアップグレードして稼働させる時になります。

*切替* という用語は、新しいシステムを稼働させる最後のプロセスに使用します。 この切替プロセスは、Microsoft Dynamics AX 2012 をオフにした後かつ Finance and Operations をオンにする前に発生するタスクで構成されます。 最終的な切替を計画する前に、[切替テスト](./upgrade-cutover-testing.md) で説明されているように、成功した切替モックを正常に完了する必要があります。

次の図は、実稼動環境で発生するような、切替中の全体的なプロセスを示しています。

![切替プロセス](./media/cutover-selfservice_01.png)

> [!NOTE]
> このトピックでは、*サンドボックス* という用語は、SQL Azure データベースに接続されている標準またはプレミア承認テスト (レベル 2 または 3)、またはより高度な環境を示します。

## <a name="overall-process"></a>全体的なプロセス

実稼動環境のアップグレード プロセスの高レベルの手順は切替モック プロセスと同じであり、詳細な指示については [AX 2012 からのアップグレード - 切替テスト (切替モック)](./upgrade-cutover-testing.md) を参照してください。


1. [データ アップグレードのアップグレード前のチェックリスト](prepare-data-upgrade.md) が完了し、カスタム コードがサンドボックス環境配置されていることを確認します。 サンドボックス環境は、データ アップグレードの場合にのみ使用する必要があります。
2. **Dynamics 365 用 AX 2012 Database Upgrade Toolkit** を、**共有資産ライブラリ > モデル** エリアの Microsoft Dynamics Lifecycle Services (LCS) からダウンロードします。 このツールキットをソースの SQL Server から使用します。
3. レプリケーションの設定を実行し、ツールキットを使用して定期的に監視を行います。
4. ダウンタイムまたはカットオーバー時で AX 2012 AOS インスタンスをオフにします。
5. レプリケーションを確実に完了してください。 このツールキットを使用し、ソースとターゲット間のレコード数を比較することで、レプリケーションの完了を検証します。 レプリケーションを検証する方法については、[アプリケーションのレポート セクション](data-upgrade-self-service.md#reporting-section-of-the-application) を参照してください。
6. ツールキットを使用してカットオーバーの手順を実行し、その完了を確認します。
7. ツールキットを使用してデータ アップグレードをトリガーし、データ アップグレードを完了します。
8. [セルフサービス データベースのプロセスを最新情報に更新](../database/database-refresh.md#self-service-database-refresh) を使用し、更新されたデータベースをサンドボックス環境から運用環境にコピーします。 
9. アプリケーションの構成を完了し、変更前のテストを完了します。
10. ユーザーが再度 Finance and Operations アプリにアクセスするようにします。


## <a name="prerequisites"></a>必要条件 
運用環境でアップグレードを実行する前に、次の前提条件を満たす必要があります。
-   サンドボックス環境でコードのアップグレードとデータのアップグレードを完了し、機能テスト パスを正常に完了します。
-   実稼働環境を配置します。 運用環境の配置を要求するオプションがオプションとなる前に、完了しておく必要があります。
    - LCS のサブスクリプション見積もりツール。 必要なスループットの詳細を提供しているため、これを使用して実稼働環境のサイズの変更を支援します。
    - LCS での手法のテスト フェーズ。 これは、プロダクション環境でテストを開始する準備ができているプロジェクトの段階にあることを確認するためです。
    - 実稼働環境を配置するために要求が Microsoft に送信された後、配置には、約 24 時間かかるので、そのために十分な時間を確保してください。
-   すべての必要な更新プログラムおよびカスタマイズ (AOT 配置可能パッケージ) を実稼動環境に適用します。 切替モックでサイン オフした後は、コードを変更しないでください。


## <a name="additional-resources"></a>追加リソース
- [Onboarding](../../fin-ops/imp-lifecycle/onboard.md)
- [データベースのセルフ サービスエ更新](../database/database-refresh.md#self-service-database-refresh)
- [AX 2012 からのアップグレード - 切替テスト (切替モック)](./upgrade-cutover-testing.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
