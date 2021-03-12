---
title: AX 2009 の移行 － マップの生成
description: このトピックは、データ マップを生成し、Microsoft Dynamics AX 2009 から Finance and Operations へデータを移行する方法を説明します。
author: kfend
manager: AnnBe
ms.date: 06/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2018-06-21
ms.dyn365.ops.version: Platform update 17
ms.openlocfilehash: 63a299be670fa31d6a40d5b1ed990e429d991eda
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679938"
---
# <a name="ax-2009-migration--generate-maps"></a>AX 2009 の移行 － マップの生成

[!include [banner](../includes/banner.md)]

Microsoft Dynamics AX 2009 から Finance and Operations へデータを移行する前に、ターゲット環境で、ソース データを配置する必要があります。 このトピックでは、ソースとターゲットのマッピングを生成する方法について説明します。

マップを生成するには、接続を検証するための対象の URL、テナント URL、およびサービス アプリケーション ID を指定する必要があります。

> [!NOTE]
> Azure ポータルの Microsoft Azure Active Directory (Azure AD) で新しいアプリケーションを作成するとき、2 つのオプション **Web API** と **ネイティブ** があります。 **ネイティブ** を選択し、ネイティブ Azure AD アプリケーションへのアクセス許可を付与します。

## <a name="prerequisites"></a>必要条件
ソース環境とターゲット環境間でデータ マップを生成する前に、データ移行ツール (DMT) をインストールする必要があります。 詳細については、 [AX 2009 の移行 - データ移行ツールのインストール](install-dmt.md) を参照してください。

## <a name="generate-maps"></a>マップの生成
データ移行のためのマップを生成するには、次の手順に従ってください。

1. AX 2009 のナビゲーション ウィンドウで、**データ移行**\>**設定** \>**接続の構成** に移動します。
2. フィールドの情報を確認して正しいことを確認し、**検証** をクリックします。
3. 検証の完了後、フォームを閉じます。
4. **設定** で、**マップを構成および生成** をクリックします。
5. フォームの情報が正しいことを確認してから、**パスの検証** をクリックします。
6. 検証が完了したら、**マップを生成** をクリックします。
