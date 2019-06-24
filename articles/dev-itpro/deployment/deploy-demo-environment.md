---
title: デモ環境の配置
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を使用して Microsoft Azure にデモ環境を配置する方法について説明します。 これは Dynamics 365 for Finance and Operations と Dynamics 365 for Retail に適用されます。
author: sarvanisathish
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 141093
ms.assetid: dcd23629-246d-4fbc-adf5-7245bb2121e4
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: 460db6ea6a5cd744a2497efc19e54c7cc1eaea5e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544223"
---
# <a name="deploy-demo-environments"></a>デモ環境の配置

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を使用して Microsoft Azure にデモ環境を配置する方法について説明します。 このトピックは、以下のデモ環境の配置に適用されます。

- Dynamics 365 for Finance and Operations
- Dynamics 365 for Retail

## <a name="prerequisites"></a>必要条件
展開を開始する前に、次の前提条件が満たされていることを確認します。

- Azure サブスクリプションがあり、そのサブスクリプションの共同管理者であることを確認します。
- LCS プロジェクトへのアクセスが可能であり、環境を展開するためのアクセス許可があることを確認します。
- [Azure Resource Manager オンボード](arm-onboarding.md) のトピックを使用して、Azure サブスクリプションが LCS プロジェクトに接続済みであることを確認します。

## <a name="deploy-a-demo-environment"></a>デモ環境の配置
LCS を使用して Azure でデモ環境を配置するには、この手順を使用します。 

1. LCS でプロジェクトを開き、**環境**セクションでプラス記号 (**+**) をクリックします。
2. Azure 環境トポロジを選択し、**デモ** を選択します。
3. トポロジを選択します。
    - Finance and Operations で、Finance and Operations 用の最新の Azure Resource Manager (ARM) トポロジを選択します。
    - 小売には、**Dynamics 365 for Retail - Demo** を選択します。
4. **環境の配置**ダイアログ ボックスに、環境の名前を入力します。 この名前は Azure サブスクリプションで一意である必要があります。 環境を簡単に識別できるようにするには、ユーザー名とトポロジを使用して略語を作成することを検討してください。
5. 仮想マシン (VM) のサイズを選択します。 ARM 用に有効になっている VM のすべてのサイズは、v2 で終わります。 Finance and Operations のワークロードには、D* v2 サイズを使用する必要があります。 D12v2 をお勧めします。
6. **インスタンス** フィールドを 1 に設定します。


~~~
**Note:** The size of the VM and the number of instances affect the cost of your subscription. For more information, see [Azure pricing](https://azure.microsoft.com/en-us/pricing/).
~~~

7. **詳細設定**をクリックし、配置にカスタマイズを追加します。 デモ環境では、既定の設定のままにすることをお勧めします。
8. ライセンスおよび価格条件に同意し、 **次へ**をクリックします。
9. **確認**メッセージ ボックスで、**配置**をクリックします。
10. 配置のステータスを表示するには、**クラウド ホスト環境**ページを開きます。 配置が正常に完了すると、環境が準備されます。

## <a name="log-on-to-your-demo-environment"></a>デモ環境へのログオン
デモ環境にログオンするには、次の手順を実行します。

1. LCS で、**クラウド ホスト環境**ページを開き、配置したデモ環境を選択します。

2. 右にスクロールし、**環境の詳細** ウィンドウの **クラウド サービス** で、適切なリンクをクリックします。

      - **Finance and Operations にログオン**
      - **小売にログオン**
