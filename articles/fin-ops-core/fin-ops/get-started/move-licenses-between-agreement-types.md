---
title: 契約タイプ間でライセンスを移動する
description: このトピックでは、契約タイプの間のライセンスを移動する方法について説明します。
author: ClaudiaBetz-Haubold
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: chaubold
ms.search.validFrom: 2018-05-30
ms.dyn365.ops.version: AX 7.0
ms.openlocfilehash: d76e4c16e551830698f2775554d7c4e18524bec8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750242"
---
# <a name="move-licenses-between-agreement-types"></a>契約タイプ間でライセンスを移動する

[!include [banner](../includes/banner.md)]

場合によっては、もともと Microsoft クラウド サービス プロバイダー (CSP) 契約を通じてサブスクリプションを購入した顧客は、Microsoft Dynamics Lifecycle Services (LCS) 実装プロジェクトが作成された後に、Microsoft との Microsoft ボリューム ライセンス契約に変更することを決定します。 顧客は、本番稼働でプロジェクトが稼動した後でもこの変更を実行できます。

ごくまれに、もともと Microsoft とのボリューム ライセンス契約を通して定期売買を購入した顧客は CSP 契約への変更することを決めます。 この場合、ボリューム ライセンス契約の更新日に合わせて変更する必要があります。

契約の 1 つのタイプから別のタイプへの定期売買契約の移動のプロセスは、主に商業プロセスです。 LCS 実装プロジェクトの技術的影響は最小限に抑えられています。

> [!NOTE]
> 契約タイプ間のサブスクリプションの移動は、Azure Active Directory (Azure AD) テナントの移動と同じではありません。 契約の契約上の変更により、 Azure AD テナントを移動する必要がある場合は、 [LCS 実装プロジェクトを別の Azure AD テナントに移動する](move-lcs-implementation-project-tenant.md) に記載されているプロセスにも従う必要があります。

サブスクリプションには、運用環境とレベル 2 スタンダード承認テスト環境の 2 つの標準環境が付属しています。 これらの環境は、契約タイプ間のサブスクリプションの移動の影響を受けません。 アクションは、顧客が追加アドオン環境を持っている場合にのみ、LCS で必要な場合があります。 この場合、アドオン環境に関連付けられているアクションには、パートナーまたは顧客リソースの側で最小限の作業量が必要になります。 環境間でデータの移動を効率化するには、最適な順序を決定するために前もって計画を作成する必要があります。

## <a name="the-customer-has-only-default-environments"></a>顧客には既定の環境のみがあります

顧客が Microsoft が管理するサブスクリプションに付属している 2 つの標準環境のみを持ち、元の CPS 契約またはボリューム ライセンス契約でアドオン環境を購入していない場合、必要な活動は純粋に商業的なものです。

1. 顧客は、ボリューム ライセンスの再販業者または CSP との新しい契約の下で定期売買を注文します。

    > [!IMPORTANT]
    > 元の契約で使用される同じ Azure AD テナントに対してサブスクリプションが購入されることを確認します。

2. 顧客によって定期売買が有効化されます。
3. Microsoft 365 管理センターで、顧客は新規のサブスクリプションおよび既存のサブスクリプションの両方が有効であることを確認します。
4. 新しいサブスクリプションが有効になると、顧客は、ボリューム ライセンスの再販業者または CSP が既存のサブスクリプションを中断することを要求します。 通常、継続性を保証し、サービスの中断を回避するために重複があります。

## <a name="the-customer-has-add-on-environments"></a>顧客にはアドオン環境があります

顧客が、元の CSP 契約またはボリューム ライセンス契約を通じてアドオン環境を購入した場合、それらの環境を再配置する必要があります。

### <a name="prerequisites"></a>必要条件

移動を開始する前に、次のタスクを行う必要があります。

- 既存の環境からデータを保存します。 [データベース移動操作ホーム ページ](../../dev-itpro/database/dbmovement-operations.md) に記載されているオプションのいずれかに従います。

- コードのすべてのパッケージが LCS で共有アセット ライブラリにアップロードされていることを確認します。

### <a name="commercial-activities"></a>商業活動

1. 顧客は、ボリューム ライセンスの再販業者または CSP との新しい契約の下で定期売買を注文します。 これらのサブスクリプションには、アドオン環境のサブスクリプションが含まれます。

    > [!IMPORTANT]
    > 既存の Azure AD テナントに対してサブスクリプションが購入されることを確認します。

2. 顧客によって定期売買が有効化されます。
3. Microsoft 365 管理センターで、顧客は新規のサブスクリプションおよび既存のサブスクリプションの両方が有効であることを確認します。

### <a name="deploy-new-environments"></a>新しい環境の配置

1. 新しいサブスクリプションが有効になると、コンフィグレーション可能な追加のアドオン環境が LCS に表示されます。 アドオン環境を配置し、適切に構成します。
2. 配置可能なパッケージを適用して、データを復元します。

### <a name="delete-environments-under-the-obsolete-agreement"></a>廃止された契約下の環境の削除

古い契約下で配置されたすべての環境で、次の手順を実行します。 環境を削除した後、再び使用したり再配置したりしないでください。

1. LCS の、**環境の詳細** ページで、**完全な詳細** を選択します。
2. 環境を停止してから、環境が停止した時に、**割り当て解除** を選択します。
3. 割り当て解除が完了したとき、**削除** を選択します。
4. 環境が削除されたら、**コンフィグレーション** を選択します。

### <a name="update-environments"></a>環境の更新

1. ボリューム ライセンスの再販業者または CSP は、既存の定期売買を中断します。
2. 元のアドオン環境は、LCS に表示されなくなります。

> [!NOTE]
> アドオン環境の物理的な再配置が完了するまでは、有効な状態にで既存の定期売買と新しい定期売買の両方をアクティブな状態に保つ必要があります。

> - サンド ボックス環境では、Azure BLOB ストレージに格納されているファイルの移動はサポートされていません。
> - コマース顧客は、移動後にコンポーネントが正常に機能するため追加の手順が必要であることに注意する必要があります。 詳細については、 [データ管理の概要](../../dev-itpro/data-entities/data-entities-data-packages.md) を参照してください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]