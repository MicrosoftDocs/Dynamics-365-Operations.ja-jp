---
title: デモ環境の配置
description: この記事では、Microsoft Dynamics Lifecycle Services (LCS) を使用して Microsoft Azure にデモ環境を配置する方法について説明します。
author: laneswenka
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.custom: 141093
ms.assetid: dcd23629-246d-4fbc-adf5-7245bb2121e4
ms.openlocfilehash: d6b8e63fe3fc33df44f74628226a5c57f34b7454
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271487"
---
# <a name="deploy-a-demo-environment"></a>デモ環境の配置

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics Lifecycle Services (LCS) を使用して Microsoft Azure にデモ環境を配置する方法について説明します。 この記事は、以下のデモ環境の配置に適用されます。

- Dynamics 365 Finance
- Dynamics 365 Supply Chain Management
- Dynamics 365 Commerce

## <a name="prerequisites"></a>必要条件
展開を開始する前に、次の前提条件が満たされていることを確認します。

- Azure サブスクリプションがあり、そのサブスクリプションの共同管理者であることを確認します。
- LCS プロジェクトへのアクセスが可能であり、環境を展開するためのアクセス許可があることを確認します。
- [Azure Resource Managerr (ARM) オンボード プロセス を完了する](arm-onboarding.md) の記事情報を参考に、Azure のサブスクリプションが LCS プロジェクトに接続済みであることを確認します。

## <a name="deploy-a-demo-environment"></a>デモ環境の配置
LCS を使用して Azure でデモ環境を配置するには、この手順を使用します。 

1. LCS でプロジェクトを開き、**環境** セクションでプラス記号 (**+**) をクリックします。
2. Azure 環境トポロジを選択し、**デモ** を選択します。
3. トポロジを選択します。
    - 財務と運用で、財務と運用向けの最新の Azure リソース マネージャー (ARM) トポロジを選択します。
    - コマースで、**Dynamics 365 for Commerce - デモ** を選択します。
4. **環境の配置** ダイアログ ボックスに、環境の名前を入力します。 この名前は Azure サブスクリプションで一意である必要があります。 環境を簡単に識別できるようにするには、ユーザー名とトポロジを使用して略語を作成することを検討してください。
5. 仮想マシン (VM) のサイズを選択します。 財務と運用のワークロードには、**Ev3 シリーズ サイズ** を使用する必要があります。 **Ev3** をお勧めします。 配賦に失敗した場合は、[Azure のトラブルシューティング ガイド](/azure/virtual-machines/troubleshooting/allocation-failure)を参照してください。
6. **インスタンス** フィールドを 1 に設定します。

    > [!NOTE] 
    > VM のサイズ と インスタンス の数は、サブスクリプションのコストに影響します。 詳細については、 [Azure の価格設定](https://azure.microsoft.com/pricing/) を参照してください。


7. **詳細設定** をクリックし、配置にカスタマイズを追加します。 デモ環境では、既定の設定のままにすることをお勧めします。
8. ライセンスおよび価格条件に同意し、 **次へ** をクリックします。
9. **確認** メッセージ ボックスで、**配置** をクリックします。
10. 配置のステータスを表示するには、**クラウド ホスト環境** ページを開きます。 配置が正常に完了すると、環境が準備されます。

## <a name="log-on-to-your-demo-environment"></a>デモ環境へのログオン
デモ環境にログオンするには、次の手順を実行します。

1. LCS で、**クラウド ホスト環境** ページを開き、配置したデモ環境を選択します。

2. 右にスクロールし、**環境の詳細** ウィンドウの **クラウド サービス** で、適切なリンクをクリックします。

      - **財務と運用にログオン**
      - **コマースにログオン**


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
