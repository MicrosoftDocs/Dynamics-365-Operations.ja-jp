---
title: AX 2009 の移行 － マップの生成
description: このトピックは、データ マップを生成し、Microsoft Dynamics AX 2009 から Finance and Operations へデータを移行する方法を説明します。
author: kfend
ms.date: 06/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2018-06-21
ms.dyn365.ops.version: Platform update 17
ms.openlocfilehash: 4ab8dca90c45bf555a7f316b20ea25200bdfcde1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751348"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]